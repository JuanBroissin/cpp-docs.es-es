---
title: Advertencia del compilador (nivel 4) C4125
ms.date: 11/04/2016
f1_keywords:
- C4125
helpviewer_keywords:
- C4125
ms.assetid: a081d1f4-0789-4915-91df-7ff0b28ca245
ms.openlocfilehash: 3b82bfd1a1acff07a0fd47bbd2abfb08178a74c6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50605366"
---
# <a name="compiler-warning-level-4-c4125"></a>Advertencia del compilador (nivel 4) C4125

el dígito decimal finaliza la secuencia de escape octal

El compilador evalúa el número octal sin el dígito decimal y supone que el dígito decimal es un carácter.

## <a name="example"></a>Ejemplo

```
// C4125a.cpp
// compile with: /W4
char array1[] = "\709"; // C4125
int main()
{
}
```

Si el dígito 9 está pensado como un carácter, corrija el ejemplo siguiente:

```
// C4125b.cpp
// compile with: /W4
char array[] = "\0709";  // C4125 String containing "89"
int main()
{
}
```