---
title: Excluir um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f39f721d434f4e54cbfa5d25a3ba626858f2b13e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583565"
---
# <a name="deleting-a-message-service"></a>Excluir um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para excluir um serviço de mensagem de um perfil**
  
1. Chame **IMAPISession::GetMsgServiceTable** para acessar a tabela de serviços de mensagem. 
    
2. Localize a linha para o serviço de mensagem e passar uma coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) no parâmetro _lpuid_ para [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** chama a função de ponto de entrada do serviço de mensagem com o parâmetro _ulContext_ definido como MSG_SERVICE_DELETE. Serviços de mensagem executam qualquer tarefas de limpeza neste momento antes de serem removidos do perfil. 
  

