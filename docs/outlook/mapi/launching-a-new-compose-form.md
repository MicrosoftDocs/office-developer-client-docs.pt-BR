---
title: Iniciar um novo formulário de redação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8d1b94c70e4de6310d2e84cf002c4e3199fced2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767777"
---
# <a name="launching-a-new-compose-form"></a>Iniciar um novo formulário de redação

  
  
**Aplica-se a**: Outlook 
  
Implementadores de servidor do formulário devem esperar que a seguinte sequência de chamadas de método em seus servidores de formulário e objetos de formulário quando um aplicativo cliente abre uma nova mensagem para redigir:
  
1. O aplicativo cliente chama o método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para obter informações sobre a classe de mensagem do servidor formulário de classe. 
    
2. O aplicativo cliente chama [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) para obter um novo objeto de formulário. 
    
3. O gerente de formulário MAPI carrega o servidor de formulário, se ele não ainda estiver na memória e obtém uma interface [IMAPIForm](imapiformiunknown.md) do servidor de formulário. 
    
4. O aplicativo cliente leva a interface **IMAPIForm** resultante e chama o método [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) para obter a interface do objeto [IPersistMessage](ipersistmessageiunknown.md) . 
    
5. O aplicativo cliente chama o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) para associar o objeto form [IMessage](imessageimapiprop.md), contexto de modo de exibição e objetos de coletor de eventos de aviso.
    
6. O aplicativo cliente chama o método de [IMAPIForm::DoVerb](imapiform-doverb.md) para invocar o verbo open. 
    
## <a name="see-also"></a>Confira também



[Interações do servidor de formulário](form-server-interactions.md)

