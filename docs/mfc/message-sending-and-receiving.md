---
title: Enviar y recibir mensajes | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- Windows messages [MFC], handling in MFC
- control-notification messages [MFC]
- messages [MFC], receiving
- messages [MFC], MFC
- MFC, messages
- messages [MFC], sending
ms.assetid: 9ce189cb-b259-4c3b-b6f2-9cfbed18b98b
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 0c587e3b84ae7afd7869a5c1405d8ddc4ab417b9
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2017
---
# <a name="message-sending-and-receiving"></a>Enviar y recibir mensajes
Tenga en cuenta la parte envía del proceso y cómo responde el marco de trabajo.  
  
 Mayoría de los mensajes resultantes de la interacción del usuario con el programa. Se generan comandos clics del mouse en los elementos de menú o botones de barra de herramientas o las pulsaciones de teclas de aceleración. El usuario también genera mensajes de Windows, por ejemplo, mover o cambiar el tamaño de una ventana. Otros mensajes de Windows se envían cuando se producen eventos como el inicio del programa o la terminación, como windows obtengan o pierden el foco y así sucesivamente. Se generan mensajes de notificación de control por clics del mouse u otras interacciones de usuario con un control, como un botón o un cuadro de lista en un cuadro de diálogo.  
  
 El **ejecutar** función miembro de clase `CWinApp` recupera los mensajes y los envía a la ventana apropiada. La mayoría de los mensajes de comandos se envían a la ventana de marco principal de la aplicación. El `WindowProc` predefinidos por la obtiene de la biblioteca de clase de los mensajes y los enruta de forma diferente, según la categoría del mensaje recibido.  
  
 Ahora considere la posibilidad de la parte receptora del proceso.  
  
 El receptor inicial de un mensaje debe ser un objeto de ventana. Mensajes de Windows normalmente se administran directamente mediante ese objeto de ventana. Mensajes de comando, que se originan normalmente en la ventana de marco principal de la aplicación, se enrutan a la cadena de destino del comando se describe en [enrutamiento de comandos](../mfc/command-routing.md).  
  
 Cada objeto capaz de recibir mensajes o comandos tiene su propio mensaje asignar que empareja un mensaje o un comando con el nombre de su controlador.  
  
 Cuando un objeto de destino del comando recibe un mensaje o un comando, busca el mapa de mensajes para una coincidencia. Si encuentra un controlador para el mensaje, llama al controlador. Para obtener más información acerca de cómo se busca en los mapas de mensajes, vea [cómo el marco de trabajo búsquedas de mapas de mensajes](../mfc/how-the-framework-searches-message-maps.md). Consulte de nuevo en la ilustración [comandos en el marco de trabajo](../mfc/user-interface-objects-and-command-ids.md).  
  
## <a name="see-also"></a>Vea también  
 [Cómo el marco llama a un controlador](../mfc/how-the-framework-calls-a-handler.md)
