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
  
Uma tabela de filas de saída contém informações sobre todas as mensagens de saída para um armazenamento de mensagens. Os provedores de armazenamento de mensagens implementam tabelas de fila de saída para o spooler MAPI usar. Os armazenamentos que não suportam o envio ou o recebimento de mensagens não precisam implementar esta tabela. 
  
Para acessar uma tabela de fila de saída, o spooler MAPI chama o método [IMsgStore::GetOutgoingQueue.](imsgstore-getoutgoingqueue.md) 
  
Há um requisito para que as mensagens sejam pré-processadas e enviadas ao provedor de transporte na mesma ordem em que foram enviadas pelo aplicativo cliente. O spooler MAPI foi projetado para aceitar mensagens do armazenamento de mensagens em ordem crescente de tempo de envio. Devido a esse requisito, pode haver algum atraso antes que algumas mensagens apareçam na tabela de filas de saída. 
  
Os armazenamentos de mensagens devem permitir a classificação na tabela de filas de saída para que o spooler MAPI possa classificar as mensagens por hora de envio ou a ordem de classificação padrão deve ser crescente no tempo de envio. 
  
A tabela de filas de saída deve enviar notificações quando o conteúdo da fila mudar.
  
As propriedades a seguir compom o conjunto de colunas necessário nas tabelas de fila de saída:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Para obter mais informações sobre como a tabela de filas de saída é usada, consulte [Enviando Mensagens Usando Provedores de Armazenamento de Mensagens.](sending-messages-by-using-message-store-providers.md)
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

