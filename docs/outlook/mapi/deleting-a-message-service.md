---
title: Excluir um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316860"
---
# <a name="deleting-a-message-service"></a>Excluir um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para excluir um serviço de mensagens de um perfil**
  
1. Chame **IMAPISession:: GetMsgServiceTable** para acessar a tabela de serviço de mensagens. 
    
2. Localize a linha do serviço de mensagens e transmita sua coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) no parâmetro _Lpuid_ para [IMsgServiceAdmin::D eletemsgservice](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** chama a função de ponto de entrada do serviço de mensagens com o parâmetro _ULCONTEXT_ definido como MSG_SERVICE_DELETE. Os serviços de mensagens realizam qualquer tarefa de limpeza no momento antes de serem removidos do perfil. 
  

