---
title: Admitir el subprocesamiento libre en un proveedor
ms.date: 11/04/2016
helpviewer_keywords:
- OLE DB providers, multithreaded
- threading [C++], providers
ms.assetid: a91270dc-cdf9-4855-88e7-88a54be7cbe8
ms.openlocfilehash: 14acaa6ad96f74b2a3f88ca366a43caa9199a1d8
ms.sourcegitcommit: 943c792fdabf01c98c31465f23949a829eab9aad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "51265040"
---
# <a name="supporting-free-threading-in-your-provider"></a>Admitir el subprocesamiento libre en un proveedor

Todas las clases de proveedor OLE DB son seguras para subprocesos y las entradas del registro se establecen en consecuencia. Es una buena idea para admitir el subprocesamiento libre para ayudar a proporcionar un alto nivel de rendimiento en situaciones multiusuario. Para ayudar a mantener su proveedor de seguros para subprocesos, debe comprobar que el código está bloqueado correctamente. Cada vez que escribe o almacena datos, debe bloquear el acceso con secciones críticas.

Cada objeto de plantilla de proveedor OLE DB tiene su propia sección crítica. Para facilitar el bloqueo, cada clase nueva que cree debe ser una clase de plantilla que toma la clase primaria nombre como argumento.

El ejemplo siguiente muestra cómo bloquear el código:

```cpp
template <class T>
class CMyObject<T> : public...

HRESULT MyObject::MyMethod(void)
{
   T* pT = (T*)this;      // this gets the parent class

// You don't need to do anything if you are only reading information

// If you want to write information, do the following:
   pT->Lock();         // engages critical section in the object
   ...;                // write whatever information you wish
   pT->Unlock();       // disengages the critical section
}
```

Para obtener más información acerca de cómo proteger las secciones críticas con `Lock` y `Unlock`, consulte [Multithreading: uso de las clases de sincronización](../../parallel/multithreading-how-to-use-the-synchronization-classes.md).

Compruebe que los métodos de invalidación (como `Execute`) son seguros para subprocesos.

## <a name="see-also"></a>Vea también

[Trabajar con plantillas de proveedores OLE DB](../../data/oledb/working-with-ole-db-provider-templates.md)