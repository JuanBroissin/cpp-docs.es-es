---
title: custom (C++)
ms.date: 11/04/2016
f1_keywords:
- vc-attr.custom
helpviewer_keywords:
- custom attributes, defining
ms.assetid: 3abac928-4d55-4ea6-8cf6-8427a4ad79f1
ms.openlocfilehash: 7aca125879591f71fe2ba60f34b712918350940f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50565703"
---
# <a name="custom-c"></a>custom (C++)

Define los metadatos de un objeto en la biblioteca de tipos.

## <a name="syntax"></a>Sintaxis

```cpp
[ custom(
   uuid,
   value
) ];
```

### <a name="parameters"></a>Parámetros

*uuid*<br/>
Identificador único.

*valor*<br/>
Un valor que se puede colocar en una variante.

## <a name="remarks"></a>Comentarios

El **personalizado** atributo de C++ hará que la información para colocarse en la biblioteca de tipos. Necesitará una herramienta que lee el valor personalizado de la biblioteca de tipos.

El **personalizado** atributo tiene la misma funcionalidad que el [personalizado](/windows/desktop/Midl/custom) atributo MIDL.

## <a name="requirements"></a>Requisitos

### <a name="attribute-context"></a>Contexto de atributo

|||
|-|-|
|**Se aplica a**|No COM **interfaz**, **clase**, **enum**s, `idl_module` métodos, los miembros de interfaz, los parámetros de la interfaz, **typedef**s, **unión**s, **struct**s|
|**Reiterativo**|Sí|
|**Atributos requeridos**|**coclase** (cuando se usa en la clase)|
|**Atributos no válidos**|Ninguna|

Para obtener más información acerca de los contextos de atributo, consulte [Contextos de atributo](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>Vea también

[Atributos IDL](idl-attributes.md)<br/>
[Atributos independientes](stand-alone-attributes.md)<br/>
[Typedef, Enum, Union y Struct (atributos)](typedef-enum-union-and-struct-attributes.md)<br/>
[Atributos de parámetro](parameter-attributes.md)<br/>
[Atributos de método](method-attributes.md)<br/>
[Atributos de clase](class-attributes.md)<br/>
[Atributos de interfaz](interface-attributes.md)