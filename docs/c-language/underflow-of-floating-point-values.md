---
title: Subdesbordamiento de valores de punto flotante
ms.date: 11/04/2016
ms.assetid: 78af8016-643c-47db-b4f1-7f06cb4b243e
ms.openlocfilehash: cd4aadc5ab006b79a43e31348fa101d40e8ca03a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50477368"
---
# <a name="underflow-of-floating-point-values"></a>Subdesbordamiento de valores de punto flotante

**ANSI 4.5.1** Si las funciones matemáticas establecen la expresión de entero `errno` en el valor de la macro `ERANGE` en errores de intervalo de subdesbordamiento

Un subdesbordamiento de punto flotante no establece la expresión `errno` en `ERANGE`. Cuando un valor se aproxima a cero y finalmente sufre subdesbordamiento, el valor se establece en cero.

## <a name="see-also"></a>Vea también

[Funciones de la biblioteca](../c-language/library-functions.md)