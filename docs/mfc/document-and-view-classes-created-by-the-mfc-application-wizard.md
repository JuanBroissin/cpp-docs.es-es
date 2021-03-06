---
title: Clases de documentos y de vistas creadas por el Asistente para aplicaciones MFC
ms.date: 11/04/2016
helpviewer_keywords:
- document classes [MFC]
- document classes [MFC], created by application wizards
- application wizards [MFC], document/view classes created
- view classes [MFC], created by application wizards
ms.assetid: 70c34a60-2701-4981-acea-c08a5787d8e6
ms.openlocfilehash: 0ef0da4ea738d02518fb68085afc194e219103cd
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50464592"
---
# <a name="document-and-view-classes-created-by-the-mfc-application-wizard"></a>Clases de documentos y de vistas creadas por el Asistente para aplicaciones MFC

MFC Application Wizard ofrece una ventaja en el desarrollo del programa mediante la creación de documento de esquema y clases de vista para usted. A continuación, puede [asignar comandos y mensajes a estas clases](../mfc/reference/mapping-messages-to-functions.md) y use el editor de código fuente de Visual C++ para escribir sus funciones miembro.

La clase de documento creada por el Asistente para aplicaciones MFC se deriva de una clase [CDocument](../mfc/reference/cdocument-class.md). Se deriva la clase de vista [CView](../mfc/reference/cview-class.md). Los nombres que el Asistente para aplicaciones proporciona estas clases y los archivos que contienen se basan en el nombre del proyecto proporcione en el cuadro de diálogo del Asistente para la aplicación. En el Asistente para la aplicación, puede usar la página clases generadas para modificar los nombres predeterminados.

Algunas aplicaciones pueden necesitar más de una clase de documento, clase de vista o clase de ventana de marco. Para obtener más información, consulte [varios tipos de documentos, vistas y marco Windows](../mfc/multiple-document-types-views-and-frame-windows.md).

## <a name="see-also"></a>Vea también

[Arquitectura documento/vista](../mfc/document-view-architecture.md)

