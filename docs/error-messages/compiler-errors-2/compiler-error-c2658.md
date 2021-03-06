---
title: Error del compilador C2658
ms.date: 11/04/2016
f1_keywords:
- C2658
helpviewer_keywords:
- C2658
ms.assetid: 638368e8-7893-4a14-abec-13c768a9543a
ms.openlocfilehash: 792fd497ad7cdb98ae72f3e6451780dad487624d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50490289"
---
# <a name="compiler-error-c2658"></a>Error del compilador C2658

'member': nueva definición en struct/union anónimas

Dos estructuras o uniones anónimas contenían declaraciones de miembros con el mismo identificador, pero con diferentes tipos. En [/Za](../../build/reference/za-ze-disable-language-extensions.md), también obtendrá este error para los miembros con el mismo identificador y tipo.

El ejemplo siguiente genera C2658:

```
// C2658.cpp
// compile with: /c
struct X {
   union { // can be struct too
      int i;
   };
   union {
      int i;   // Under /Za, C2658
      // int i not needed here because it is defined in the first union
   };
};

struct Z {
   union {
      char *i;
   };

   union {
      void *i;   // C2658 redefinition of 'i'
      // try the following line instead
      // void *ii;
   };
};
```