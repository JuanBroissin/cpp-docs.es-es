---
title: library_block (atributo de COM de C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.library_block
helpviewer_keywords:
- library_block attribute
ms.assetid: ae7a7ebe-5e1a-4eda-a058-11bbd058ece8
ms.openlocfilehash: 76e643cb45d8a87408015e6e0726e47d423147f1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50459931"
---
# <a name="libraryblock"></a>library_block

Coloca una construcción dentro del bloque de biblioteca IDL.

## <a name="syntax"></a>Sintaxis

```cpp
[library_block]
```

## <a name="remarks"></a>Comentarios

Cuando se coloca una construcción dentro del bloque de biblioteca, asegúrese de que se pasarán en la biblioteca de tipos, independientemente de si se hace referencia. De forma predeterminada, solo construcciones modificación el [coclase](coclass.md), [dispinterface](dispinterface.md), y [idl_module](idl-module.md) atributos se colocan en el bloque de biblioteca.

## <a name="example"></a>Ejemplo

En el código siguiente, se coloca una interfaz personalizada dentro del bloque de biblioteca.

```cpp
// cpp_attr_ref_library_block.cpp
// compile with: /LD
#include <windows.h>
[module(name="MyLib")];
[object, library_block, uuid("9E66A290-4365-11D2-A997-00C04FA37DDB")]
__interface IMyInterface {
   HRESULT f1();
};
```

## <a name="requirements"></a>Requisitos

### <a name="attribute-context"></a>Contexto de atributo

|||
|-|-|
|**Se aplica a**|En cualquier lugar|
|**Reiterativo**|No|
|**Atributos requeridos**|Ninguna|
|**Atributos no válidos**|Ninguna|

Para obtener más información, vea [Contextos de atributo](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>Vea también

[Atributos de compilador](compiler-attributes.md)<br/>
[Atributos independientes](stand-alone-attributes.md)