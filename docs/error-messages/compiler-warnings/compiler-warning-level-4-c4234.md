---
title: Advertencia del compilador (nivel 4) C4234
ms.date: 11/04/2016
f1_keywords:
- C4234
helpviewer_keywords:
- C4234
ms.assetid: f7fecd5c-8248-4fde-8446-502aedc357ca
ms.openlocfilehash: 314ee068fb2be6148304360b0aaa3bd8029c283b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50441020"
---
# <a name="compiler-warning-level-4-c4234"></a>Advertencia del compilador (nivel 4) C4234

ha utilizado una extensión no estándar:' palabra clave reservada para uso futuro

El compilador aún no implementa la palabra clave utilizada.

Esta advertencia suele convertirse automáticamente en un error. Si desea modificar este comportamiento, use [advertencia #pragma](../../preprocessor/warning.md). Por ejemplo, para convertir C4234 en una advertencia de nivel 4

```
#pragma warning(2:4234)
```

en el archivo de código fuente.