---
title: Orden de las opciones de CL
ms.date: 11/04/2016
f1_keywords:
- cl
helpviewer_keywords:
- cl.exe compiler, setting options
ms.assetid: 300908ce-ae00-4b45-964b-e4e69ff6777b
ms.openlocfilehash: e5dd07f52f853b17bf663e2fbad7dbe66a3a1db7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50633545"
---
# <a name="order-of-cl-options"></a>Orden de las opciones de CL

Las opciones pueden aparecer en cualquier lugar en la línea de comandos de CL, excepto la opción /link, que debe aparecer en último lugar. El compilador comienza con las opciones especificadas en el [variable de entorno de CL](../../build/reference/cl-environment-variables.md) y, a continuación, lee la línea de comandos de izquierda a derecha: procesamiento de archivos de comandos en el orden en que los encuentra. Cada opción se aplica a todos los archivos en la línea de comandos. Si CL encuentra opciones en conflicto, utiliza la opción más a la derecha.

## <a name="see-also"></a>Vea también

[Sintaxis de la línea de comandos del compilador](../../build/reference/compiler-command-line-syntax.md)