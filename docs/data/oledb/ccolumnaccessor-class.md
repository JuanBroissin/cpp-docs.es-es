---
title: CColumnAccessor (Clase)
ms.date: 11/04/2016
f1_keywords:
- CColumnAccessor
- ATL::CColumnAccessor
- ATL.CColumnAccessor
helpviewer_keywords:
- CColumnAccessor class
ms.assetid: 6ce1e67f-6a20-490d-9326-c168b43eee7e
ms.openlocfilehash: 85d3d9d4339634ea7948d7d5e9e09725b7fd8758
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50611373"
---
# <a name="ccolumnaccessor-class"></a>CColumnAccessor (Clase)

Genera código insertado de consumidor.

## <a name="syntax"></a>Sintaxis

```cpp
class CColumnAccessor : public CAccessorBase
```

## <a name="remarks"></a>Comentarios

En el código insertado, cada columna se enlaza como un descriptor de acceso independiente. Debe tener en cuenta que esta clase se usa en el código insertado (por ejemplo, es posible que aparece al depurar), pero normalmente nunca tendrá que utilizarla o sus métodos directamente.

`CColumnAccessor` implementa los siguientes métodos de código auxiliar, cada uno de los cuales corresponden de funcionalidad a otros métodos de clase de descriptor de acceso:

- `CColumnAccessor` El constructor; crea una instancia e inicializa el `CColumnAccessor` objeto.

- `CreateAccessor` Asigna memoria para la columna de las estructuras de enlace e inicializa a los miembros de datos de columna.

- `BindColumns` Enlaza las columnas a los descriptores de acceso.

- `SetParameterBuffer` Asigna los búferes de parámetros.

- `AddParameter` Agrega una entrada de parámetro a las estructuras de entrada de parámetro.

- `HasOutputColumns` Determina si el descriptor de acceso tiene columnas de salida

- `HasParameters` Determina si el descriptor de acceso tiene parámetros.

- `BindParameters` Enlaza los parámetros creados para las columnas.

## <a name="requirements"></a>Requisitos

**Encabezado:** atldbcli.h

## <a name="see-also"></a>Vea también

[Plantillas de consumidor OLE DB](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Referencia de plantillas de consumidor OLE DB](../../data/oledb/ole-db-consumer-templates-reference.md)