---
title: Error irrecuperable C1070
ms.date: 11/04/2016
f1_keywords:
- C1070
helpviewer_keywords:
- C1070
ms.assetid: 1058269a-5db6-4c23-a97f-b5269eb9188b
ms.openlocfilehash: 7e156a230ce9550b65d1b8775947fc7294c15377
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50445024"
---
# <a name="fatal-error-c1070"></a>Error irrecuperable C1070

el par #if/#endif no coincide en el archivo 'filename'

Una directiva `#if`, `#ifdef`, o `#ifndef` no tiene ningún correspondiente `#endif`.

El ejemplo siguiente genera la advertencia C1070:

```
// C1070.cpp
#define TEST

#ifdef TEST

#ifdef TEST
#endif
// C1070
```

Posible solución:

```
// C1070b.cpp
// compile with: /c
#define TEST

#ifdef TEST
#endif

#ifdef TEST
#endif
```