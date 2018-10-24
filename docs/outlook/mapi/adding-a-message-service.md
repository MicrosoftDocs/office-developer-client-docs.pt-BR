---
title: Adicionar um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6a8b0f8fc8c296fe4022ac28623b83d270472ca3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590691"
---
# <a name="adding-a-message-service"></a>Adicionar um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para adicionar um novo serviço de mensagem a um perfil e acessar o novo serviço de mensagem**
  
Chame [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** executa as seguintes tarefas: 
  
1. Copia todas as informações relevantes para o serviço de mensagem que está no MAPISVC. Arquivo INF, criando uma seção de perfil para cada seção do provedor.
    
2. Chama a função de ponto de entrada do serviço de mensagem, **MSGSERVICEENTRY**, com o parâmetro _ulContext_ definido como MSG_SERVICE_CREATE. 
    
3. Define e recupera a mensagem propriedade do serviço **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).
    
 **Para acessar qualquer serviço recém-adicionado mensagem**
  
1. Chame [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar a tabela de serviços de mensagem. 
    
2. Chame o método de [IMAPITable::Advise](imapitable-advise.md) de tabela serviço de mensagens para registrar para notificações de tabela. 
    
3. Quando MAPI envia uma notificação TABLE_ROW_ADDED, localize o identificador de entrada do serviço recém-adicionado mensagem na estrutura [SRow](srow.md) incluída na estrutura de [TABLE_NOTIFICATION](table_notification.md) . 
    

