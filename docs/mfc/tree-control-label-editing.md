---
title: Edición de etiquetas de control de árbol
ms.date: 11/04/2016
helpviewer_keywords:
- editing tree control labels
- CTreeCtrl class [MFC], editing labels
- label editing in CTreeCtrl class [MFC]
- tree controls [MFC], label editing
ms.assetid: 6cde2ac3-43ee-468f-bac2-cf1a228ad32d
ms.openlocfilehash: 80d4f37ef8b67c2902e5d34cb4ec8aa4cf35a616
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50647998"
---
# <a name="tree-control-label-editing"></a>Edición de etiquetas de control de árbol

El usuario puede editar directamente las etiquetas de elementos de un control de árbol ([CTreeCtrl](../mfc/reference/ctreectrl-class.md)) que tiene el **TVS_EDITLABELS** estilo. El usuario comienza a editar, haga clic en la etiqueta del elemento que tiene el foco. Una aplicación comienza a editar mediante el uso de la [función miembro EditLabel](../mfc/reference/ctreectrl-class.md#editlabel) función miembro. El control de árbol envía la notificación al editar comienza y cuando se cancela o completa. Cuando se completa la edición, usted es responsable de actualizar la etiqueta del elemento, si procede.

Cuando etiqueta comienza la edición, un control de árbol envía un [TVN_BEGINLABELEDIT](/windows/desktop/Controls/tvn-beginlabeledit) mensaje de notificación. Mediante el procesamiento de esta notificación, puede permitir la edición de algunas etiquetas y evitar las modificaciones de los demás. Devolver 0 permite la edición y devolver distinto de cero evita.

Cuando la edición de la etiqueta de cancelarla o completarla, un control de árbol envía un [TVN_ENDLABELEDIT](/windows/desktop/Controls/tvn-endlabeledit) mensaje de notificación. El *lParam* parámetro es la dirección de un [estructura NMTVDISPINFO](/windows/desktop/api/commctrl/ns-commctrl-tagtvdispinfoa) estructura. El **elemento** miembro es un [estructura TVITEM](/windows/desktop/api/commctrl/ns-commctrl-tagtvitema) estructura que identifica el elemento e incluye el texto editado. Usted es responsable de actualizar la etiqueta del elemento, si es necesario, tal vez después de validar la cadena editada. El *pszText* miembro de `TV_ITEM` es 0 si se cancela la edición.

Durante la edición de etiquetas, normalmente en respuesta a la [TVN_BEGINLABELEDIT](/windows/desktop/Controls/tvn-beginlabeledit) mensaje de notificación, puede obtener un puntero para el control de edición que se usa para editar etiquetas mediante el uso de la [función miembro GetEditControl](../mfc/reference/ctreectrl-class.md#geteditcontrol) miembro función. Puede llamar el control de edición [SetLimitText](../mfc/reference/cedit-class.md#setlimittext) función miembro para limitar la cantidad de texto que un usuario puede escribir o subclase el control de edición para interceptar y descartar los caracteres no válidos. Sin embargo, tenga en cuenta que el control de edición se muestra solo *después* **TVN_BEGINLABELEDIT** se envía.

## <a name="see-also"></a>Vea también

[Uso de CTreeCtrl](../mfc/using-ctreectrl.md)<br/>
[Controles](../mfc/controls-mfc.md)

