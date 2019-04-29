---
title: Tabelas de fila de saída
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437571"
---
# <a name="outgoing-queue-tables"></a>Tabelas de fila de saída

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de fila de saída contém informações sobre todas as mensagens de saída de um repositório de mensagens. Os provedores de repositório de mensagens implementam tabelas de fila de saída para o spooler MAPI a ser usado. Os repositórios que não dão suporte ao envio ou recebimento de mensagens não precisam implementar essa tabela. 
  
Para acessar uma tabela de fila de saída, o spooler MAPI chama o método [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md) . 
  
Há um requisito de que as mensagens sejam preprocessadas e enviadas ao provedor de transporte na mesma ordem em que foram enviadas pelo aplicativo cliente. O MAPI spooler é projetado para aceitar mensagens do repositório de mensagens em ordem crescente de tempo de envio. Devido a esse requisito, pode haver um atraso antes de algumas mensagens aparecerem na tabela de fila de saída. 
  
Os repositórios de mensagens devem permitir a classificação na tabela de fila de saída para que o spooler MAPI possa classificar as mensagens por hora de envio ou a ordem de classificação padrão deve ser em tempo de envio em ordem crescente. 
  
A tabela de fila de saída deve enviar notificações quando o conteúdo da fila é alterado.
  
As propriedades a seguir compõem o conjunto de colunas necessárias nas tabelas de fila de saída:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Para obter mais informações sobre como a tabela de fila de saída é usada, consulte [enviando mensagens usando provedores de repositório de mensagens](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

