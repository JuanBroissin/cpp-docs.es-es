---
title: Administración de memoria con CStringT
ms.date: 11/04/2016
f1_keywords:
- CStringT
- ATL::CStringT
- ATL.CStringT
helpviewer_keywords:
- CString objects, memory management
- memory [C++], usage
- IAtlStringMgr class, using
- strings [C++], custom memory management
- CFixedStringT class, description of
- strings [C++], memory management
- CStringT class, memory management
ms.assetid: 88b8342d-19b5-48c4-9cf6-e4c44cece21e
ms.openlocfilehash: f45aac11f0c42aecf8c72cf6f7d1630d50b780f3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50598030"
---
# <a name="memory-management-with-cstringt"></a>Administración de memoria con CStringT

Clase [CStringT](../atl-mfc-shared/reference/cstringt-class.md) es una clase de plantilla utilizada para manipular las cadenas de caracteres de longitud variable. Se asignan y liberan a través de un objeto de administrador de cadenas, asociado con cada instancia de la memoria para almacenar estas cadenas `CStringT`. MFC y ATL proporcionan instancias predeterminadas de `CStringT`, llamado `CString`, `CStringA`, y `CStringW`, que manipulan cadenas de distintos tipos de caracteres. Estos tipos de caracteres son de tipo TCHAR, **char**, y `wchar_t`, respectivamente. Estos tipos de cadena predeterminada usan un administrador de cadenas que asigna memoria del montón del proceso (en ATL) o el montón de CRT (en MFC). Para las aplicaciones típicas, este esquema de asignación de memoria es suficiente. Sin embargo, para el código que hace uso intensivo uso de cadenas (o código multiproceso) los administradores de memoria predeterminada no pueden realizar de forma óptima. Este tema describe cómo invalidar el comportamiento predeterminado de administración de memoria de `CStringT`, creando asignadores específicamente optimizado para la tarea en cuestión.

- [Implementación de un administrador de cadenas personalizado (método básico)](../atl-mfc-shared/implementation-of-a-custom-string-manager-basic-method.md)

- [Evitar la contención del montón](../atl-mfc-shared/avoidance-of-heap-contention.md)

- [Implementación de un administrador de cadenas personalizado (método avanzado)](../atl-mfc-shared/implementation-of-a-custom-string-manager-advanced-method.md)

- [CFixedStringT: Un ejemplo de un administrador de cadenas personalizado](../atl-mfc-shared/cfixedstringt-example-of-a-custom-string-manager.md)

## <a name="see-also"></a>Vea también

[Ejemplo CustomString](../visual-cpp-samples.md)

