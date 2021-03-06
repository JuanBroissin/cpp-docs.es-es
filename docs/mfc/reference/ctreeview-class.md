---
title: Clase CTreeView
ms.date: 11/04/2016
f1_keywords:
- CTreeView
- AFXCVIEW/CTreeView
- AFXCVIEW/CTreeView::CTreeView
- AFXCVIEW/CTreeView::GetTreeCtrl
helpviewer_keywords:
- CTreeView [MFC], CTreeView
- CTreeView [MFC], GetTreeCtrl
ms.assetid: 5df583a6-d69f-42ca-9d8d-57e04558afff
ms.openlocfilehash: db899b58c68dabc25e571c390db0575a2d2ebb58
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50496350"
---
# <a name="ctreeview-class"></a>Clase CTreeView

Simplifica el uso del control de árbol y de [CTreeCtrl](../../mfc/reference/ctreectrl-class.md), la clase que encapsula la funcionalidad de control de árbol, con la arquitectura de vista-documento de MFC.

## <a name="syntax"></a>Sintaxis

```
class CTreeView : public CCtrlView
```

## <a name="members"></a>Miembros

### <a name="public-constructors"></a>Constructores públicos

|Name|Descripción|
|----------|-----------------|
|[CTreeView::CTreeView](#ctreeview)|Construye un objeto `CTreeView`.|

### <a name="public-methods"></a>Métodos públicos

|Name|Descripción|
|----------|-----------------|
|[CTreeView:: GetTreeCtrl](#gettreectrl)|Devuelve el control de árbol asociado a la vista.|

## <a name="remarks"></a>Comentarios

Para obtener más información acerca de esta arquitectura, consulte la información general de la [CView](../../mfc/reference/cview-class.md) clase y las referencias cruzadas citadas no existe.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CView](../../mfc/reference/cview-class.md)

[CCtrlView](../../mfc/reference/cctrlview-class.md)

`CTreeView`

## <a name="requirements"></a>Requisitos

**Encabezado:** afxcview.h

##  <a name="ctreeview"></a>  CTreeView::CTreeView

Construye un objeto `CTreeView`.

```
CTreeView();
```

##  <a name="gettreectrl"></a>  CTreeView:: GetTreeCtrl

Devuelve una referencia al control de árbol asociado a la vista.

```
CTreeCtrl& GetTreeCtrl() const;
```

## <a name="see-also"></a>Vea también

[CCtrlView (clase)](../../mfc/reference/cctrlview-class.md)<br/>
[Gráfico de jerarquías](../../mfc/hierarchy-chart.md)<br/>
[CView (clase)](../../mfc/reference/cview-class.md)<br/>
[CCtrlView (clase)](../../mfc/reference/cctrlview-class.md)<br/>
[CTreeCtrl (clase)](../../mfc/reference/ctreectrl-class.md)
