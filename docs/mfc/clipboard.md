---
title: Portapapeles
ms.date: 11/04/2016
helpviewer_keywords:
- cutting and copying data
- copying data
- Clipboard
- Clipboard, programming
- transferring data
ms.assetid: a71b2824-1f14-4914-8816-54578d73ad4e
ms.openlocfilehash: b17268c78fb5e82cbe75cbe0647b931d06934ef1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50440799"
---
# <a name="clipboard"></a>Portapapeles

Esta serie de artículos explica cómo implementar la compatibilidad con el Portapapeles de Windows en aplicaciones MFC. El Portapapeles de Windows se utiliza de dos maneras:

- Implementación de comandos del menú Edición estándares, como cortar, copiar y pegar.

- Implementación de datos uniforme transferir con arrastrar y colocar (OLE).

El Portapapeles es el método de Windows estándar de transferencia de datos entre un origen y un destino. También puede ser muy útil en operaciones de OLE. Con la llegada de OLE, hay dos mecanismos de Portapapeles de Windows. La API de Portapapeles de Windows estándar sigue estando disponible, pero se ha complementado con el mecanismo de transferencia de datos OLE. Transferencia de datos uniforme OLE (UDT) es compatible con Cortar, copiar y pegar en el Portapapeles y arrastrar y colocar.

El Portapapeles es un servicio de sistema compartido por toda la sesión de Windows, por lo que no tiene un identificador o una clase propia. Administrar el Portapapeles mediante funciones miembro de clase [CWnd](../mfc/reference/cwnd-class.md).

## <a name="what-do-you-want-to-know-more-about"></a>¿Qué desea saber más sobre

- [Cuándo usar cada mecanismo del Portapapeles](../mfc/clipboard-when-to-use-each-clipboard-mechanism.md)

- [Mediante la API de Portapapeles de Windows tradicional](../mfc/clipboard-using-the-windows-clipboard.md)

- [Mediante el mecanismo del Portapapeles de OLE](../mfc/clipboard-using-the-ole-clipboard-mechanism.md)

- [Copiar y pegar datos](../mfc/clipboard-copying-and-pasting-data.md)

- [Agregar otros formatos](../mfc/clipboard-adding-other-formats.md)

- [El Portapapeles de Windows](https://msdn.microsoft.com/library/ms648709)

- [Implementación de arrastrar y colocar (OLE)](../mfc/drag-and-drop-ole.md)

## <a name="see-also"></a>Vea también

[Elementos de la interfaz de usuario](../mfc/user-interface-elements-mfc.md)
