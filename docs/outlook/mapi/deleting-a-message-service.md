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
ms.openlocfilehash: 34d9d6d428f39765e739ce856f3666d07b457d52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766392"
---
# <a name="deleting-a-message-service"></a>Excluir um serviço de mensagens

  
  
**Aplica-se a**: Outlook 
  
 **Para excluir um serviço de mensagem de um perfil**
  
1. Chame **IMAPISession::GetMsgServiceTable** para acessar a tabela de serviços de mensagem. 
    
2. Localize a linha para o serviço de mensagem e passar uma coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) no parâmetro _lpuid_ para [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** chama a função de ponto de entrada do serviço de mensagem com o parâmetro _ulContext_ definido como MSG_SERVICE_DELETE. Serviços de mensagem executam qualquer tarefas de limpeza neste momento antes de serem removidos do perfil. 
  

