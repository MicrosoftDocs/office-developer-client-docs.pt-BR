---
title: Adicionar um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a7735be5cfb8ff0716b6bd6eba4951563bb938ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766118"
---
# <a name="adding-a-message-service"></a>Adicionar um serviço de mensagens

  
  
**Aplica-se a**: Outlook 
  
 **Para adicionar um novo serviço de mensagem a um perfil e acessar o novo serviço de mensagem**
  
Chame [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** executa as seguintes tarefas: 
  
1. Copia todas as informações relevantes para o serviço de mensagem que está no MAPISVC. Arquivo INF, criando uma seção de perfil para cada seção do provedor.
    
2. Chama a função de ponto de entrada do serviço de mensagem, **MSGSERVICEENTRY**, com o parâmetro _ulContext_ definido como MSG_SERVICE_CREATE. 
    
3. Define e recupera a mensagem propriedade do serviço **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).
    
 **Para acessar qualquer serviço recém-adicionado mensagem**
  
1. Chame [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar a tabela de serviços de mensagem. 
    
2. Chame o método de [IMAPITable::Advise](imapitable-advise.md) de tabela serviço de mensagens para registrar para notificações de tabela. 
    
3. Quando MAPI envia uma notificação TABLE_ROW_ADDED, localize o identificador de entrada do serviço recém-adicionado mensagem na estrutura [SRow](srow.md) incluída na estrutura de [TABLE_NOTIFICATION](table_notification.md) . 
    

