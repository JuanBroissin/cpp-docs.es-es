---
title: Error del compilador C3292
ms.date: 11/04/2016
f1_keywords:
- C3292
helpviewer_keywords:
- C3292
ms.assetid: ead485cc-5471-4e10-b361-300589ff5b70
ms.openlocfilehash: 7c59932a79534a365a20fcad25583f7addc0d624
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50609615"
---
# <a name="compiler-error-c3292"></a>Error del compilador C3292

el espacio de nombres cli no se puede abrir de nuevo

El espacio de nombres cli no se puede declarar en su código.  Para obtener más información, consulte [de plataforma, predeterminado y cli de espacios de nombres](../../windows/platform-default-and-cli-namespaces-cpp-component-extensions.md).

## <a name="example"></a>Ejemplo

El ejemplo siguiente genera la advertencia C3292.

```
// C3292.cpp
// compile with: /clr /c
namespace cli {};   // C3292
```