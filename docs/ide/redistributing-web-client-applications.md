---
title: Redistribuir aplicaciones cliente web
ms.date: 11/04/2016
helpviewer_keywords:
- Web applications [C++], redistributing
- deploying applications [C++], Web applications
- Internet applications [C++], redistributing
- application deployment [C++], Web applications
ms.assetid: fe05988b-dee8-4a46-b381-016b5103a6bf
ms.openlocfilehash: 37ff666493ada7dada19f5731e6581603d3cb57e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50512425"
---
# <a name="redistributing-web-client-applications"></a>Redistribuir aplicaciones cliente web

Si en la aplicación se usan las clases de MFC que implementan el control WebBrowser (por ejemplo, `CHtmlView` o `CHtmlEditView`), en el equipo de destino debe estar instalado Microsoft Internet Explorer 4.0 o una versión posterior como mínimo.

Instalar la versión más reciente de Internet Explorer también garantiza que el equipo de destino tiene los archivos de control comunes más recientes. Para obtener más información, vea [Instalar e implementar Internet Explorer 11](/internet-explorer/ie11-deploy-guide/install-and-deploy-ie11).

## <a name="see-also"></a>Vea también

[Implementar aplicaciones de escritorio](../ide/deploying-native-desktop-applications-visual-cpp.md)