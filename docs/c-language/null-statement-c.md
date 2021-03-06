---
title: NULL (Instrucción) (C)
ms.date: 11/04/2016
helpviewer_keywords:
- semicolon, C null statement
- expressions [C++], null
- null statement
- null values, expressions
ms.assetid: 72576ce6-26d0-4379-be65-fee522088790
ms.openlocfilehash: bee044049ed14796a97edc62bbb180ab19700564
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50503057"
---
# <a name="null-statement-c"></a>NULL (Instrucción) (C)

Una "instrucción null" es una instrucción que solo contiene un punto y coma; puede aparecer en cualquier lugar donde se espere una instrucción. No ocurre nada cuando se ejecuta una instrucción null. La manera correcta de escribir una instrucción null es:

## <a name="syntax"></a>Sintaxis

> **;**

## <a name="remarks"></a>Comentarios

Las instrucciones como **do**, **for**, **if** y `while` requieren que aparezca una instrucción ejecutable como cuerpo de la instrucción. La instrucción null cumple el requisito sintáctico en los casos en que no se necesita un cuerpo de instrucción sustancial.

Como con cualquier otra instrucción de C, puede incluir una etiqueta delante de una instrucción null. Para etiquetar un elemento que no es una instrucción, como la llave de cierre de una instrucción compuesta, puede etiquetar una instrucción null e insertarla inmediatamente delante del elemento para obtener el mismo efecto.

En este ejemplo se ilustra la instrucción null:

```C
for ( i = 0; i < 10; line[i++] = 0 )
     ;
```

En este ejemplo, la expresión de bucle de la instrucción **for** `line[i++] = 0` inicializa los 10 primeros elementos de `line` en 0. El cuerpo de la instrucción es una instrucción null, ya que no se requieren más instrucciones.

## <a name="see-also"></a>Vea también

[Instrucciones](../c-language/statements-c.md)