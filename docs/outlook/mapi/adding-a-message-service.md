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
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407232"
---
# <a name="adding-a-message-service"></a>Adicionar um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para adicionar um novo serviço de mensagens a um perfil e acessar o novo serviço de mensagens**
  
Chamar [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). O **CreateMsgServiceEx** executa as seguintes tarefas: 
  
1. Copia todas as informações relevantes para o serviço de mensagens que está no MAPISVC. Arquivo INF, criando uma seção de perfil para cada seção de provedor.
    
2. Chama a função de ponto de entrada do serviço de mensagens, **MSGSERVICEENTRY**, com o parâmetro _ULCONTEXT_ definido como MSG_SERVICE_CREATE. 
    
3. Define e recupera a propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) do serviço de mensagens.
    
 **Para acessar qualquer serviço de mensagens recém-adicionado**
  
1. Chame [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar a tabela de serviço de mensagens. 
    
2. Chame o método imApitable [:: Advise](imapitable-advise.md) da tabela de serviço de mensagens para se registrar para notificações de tabela. 
    
3. Quando MAPI envia uma notificação TABLE_ROW_ADDED, localize o identificador de entrada do serviço de mensagens recém-adicionado na estrutura [SRow](srow.md) incluída na estrutura [TABLE_NOTIFICATION](table_notification.md) . 
    

