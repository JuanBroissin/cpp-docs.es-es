---
title: Destruir el control de lista
ms.date: 11/04/2016
helpviewer_keywords:
- list controls [MFC], destroying
- CListCtrl class [MFC], destroying controls
ms.assetid: 513ec820-3a02-49d2-b073-a6a7a3fc91b3
ms.openlocfilehash: 85089919ccb81003dad1eab439fa8a0d127fd9ff
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50568355"
---
# <a name="destroying-the-list-control"></a>Destruir el control de lista

Si incrusta la [CListCtrl](../mfc/reference/clistctrl-class.md) objeto como un miembro de datos de una clase de vista o cuadro de diálogo, se destruye cuando se destruye su propietario. Si usa un [CListView](../mfc/reference/clistview-class.md), el marco de trabajo destruye el control cuando se destruye la vista.

Si organizas para algunos de los datos de lista que se almacenará en la aplicación en lugar del control de lista, deberá desasignarlos. Para obtener más información, consulte [elementos de devolución de llamada y máscara de devolución de llamada](/windows/desktop/Controls/using-list-view-controls) en el SDK de Windows.

Además, usted es responsable de desasignar las listas de imágenes creado y asociado al objeto de control de lista.

## <a name="see-also"></a>Vea también

[Uso de CListCtrl](../mfc/using-clistctrl.md)<br/>
[Controles](../mfc/controls-mfc.md)

