---
title: Error del compilador C2474
ms.date: 11/04/2016
f1_keywords:
- C2474
helpviewer_keywords:
- C2474
ms.assetid: 64e6c61e-6e77-480e-bcf0-b30a2fc482ac
ms.openlocfilehash: c49f38b828a41c72135ba9182d4d0f5eee4df1de
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50475314"
---
# <a name="compiler-error-c2474"></a>Error del compilador C2474

'keyword': falta un punto y coma adyacente que podría ser una palabra clave o un identificador.

El compilador esperaba encontrar un punto y coma y no pudo determinar su intención. Agregue el punto y coma para solucionar este error.

## <a name="example"></a>Ejemplo

El ejemplo siguiente genera la advertencia C2474.

```
// C2474.cpp
// compile with: /clr /c

ref class A {
   ref class B {}
   property int i;   // C2474 error
};

// OK
ref class B {
   ref class D {};
   property int i;
};

ref class E {
   ref class F {} property;
   int i;
};
```