---
title: Tabelas de filas de saída
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c5f136a0d26b7519bc1b7b3d8f448f5f382767ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591251"
---
# <a name="outgoing-queue-tables"></a>Tabelas de filas de saída

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de fila de saída contém informações sobre todas as mensagens de saída para um armazenamento de mensagens. Provedores de armazenamento de mensagem implementam tabelas de fila de saída para o MAPI spooler usar. Repositórios que não têm suporte para o envio ou recebimento de mensagens não precisa implementar nesta tabela. 
  
Para acessar uma tabela de fila de saída, o MAPI spooler chama o método [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) . 
  
Não há um requisito para que as mensagens sejam preprocessadas e enviadas para o provedor de transporte na mesma ordem em que foram enviadas pelo aplicativo cliente. O MAPI spooler foi projetado para aceitar mensagens de armazenamento de mensagens em ordem crescente de tempo de envio. Devido a esse requisito, pode haver algumas atraso antes de algumas mensagens aparecem na tabela de fila de saída. 
  
Repositórios de mensagem seja devem permitir a classificação na tabela de fila de saída para que o MAPI spooler pode classificar as mensagens por hora de envio, ou a ordem de classificação padrão deve ser por hora de envio de em ordem crescente. 
  
A tabela de fila de saída deve enviar notificações quando o conteúdo da fila é alterado.
  
As seguintes propriedades compõem a coluna necessária definida nas tabelas de fila de saída:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Para obter mais informações sobre como a tabela de fila de saída é usada, consulte [Enviando mensagens por provedores de repositório de mensagem usando](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

