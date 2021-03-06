---
title: Evaluación de tokens
ms.date: 11/04/2016
helpviewer_keywords:
- tokens, evaluating
ms.assetid: 28870b62-dff6-4644-8b75-d58f340b48d2
ms.openlocfilehash: c54b497464d68a9e6c6048a93119726e14ef4718
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50482061"
---
# <a name="evaluation-of-tokens"></a>Evaluación de tokens

Cuando el compilador interpreta tokens, incluye todos los caracteres posibles en un único token antes de pasar al token siguiente. Debido a este comportamiento, el compilador no puede interpretar los tokens tal como se pretende cuando no están correctamente separados por espacio en blanco. Observe la siguiente expresión:

```
i+++j
```

En este ejemplo, el compilador crea primero el operador más largo posible (`++`) de los tres signos más y, después, procesa el signo más restante como operador de suma (`+`). Así, la expresión se interpreta como `(i++) + (j)`, no `(i) + (++j)`. En este caso y otros similares, utilice el espacio en blanco y paréntesis para evitar la ambigüedad y garantizar la evaluación adecuada de la expresión.

**Específicos de Microsoft**

El compilador de C trata un carácter CTRL+Z como un indicador de fin de archivo. Omite cualquier texto después de CTRL+Z.

**FIN de Específicos de Microsoft**

## <a name="see-also"></a>Vea también

[Tokens de C](../c-language/c-tokens.md)