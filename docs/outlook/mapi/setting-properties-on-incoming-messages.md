---
title: Definir propriedades em mensagens de entrada
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 44b5b489d3efce3ecea69ccd8b7b7a638b173c13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578433"
---
# <a name="setting-properties-on-incoming-messages"></a>Definir propriedades em mensagens de entrada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente do interior do subsistema MAPI esperam um número de propriedades em qualquer mensagem recebida. Quando o provedor de transporte traz uma mensagem para o MAPI, ele deve definir essas propriedades, pois ele é o único processo com as informações necessárias para fazê-lo ou pelo menos é a melhor fonte das informações.
  
Provedores são incentivados a definir os valores para todas essas propriedades nas mensagens de entrada.
  
|**Nome da propriedade**|**Descrição**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |O assunto da mensagem.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Texto da mensagem de texto sem formatação.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Texto da mensagem RTF compactado.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |A data e hora que a mensagem foi entregue.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |O nome de exibição do originador mensagem.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |A entrada do catálogo de endereços do originador mensagem.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |A chave de pesquisa de catálogo de endereços do originador mensagem.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |A hora em que a mensagem foi enviada com seu sistema de mensagens pelo cliente de mensagens do remetente.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |O nome do delegado representativo para enviar.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |A entrada do catálogo de endereços do envio delegado.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |A chave de pesquisa de catálogo de endereços do envio delegado.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |O nome do delegado representativo para receber.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |A entrada do catálogo de endereços do recebimento delegado.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |A chave de pesquisa de catálogo de endereços do recebimento delegado.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |A lista do destinatário delegada exibir nomes, separados por uma vírgula e um espaço (";").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |A lista de destinatários delegadas por uma resposta.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Indica que o destinatário foi especificamente nomeado como um destinatário "para" (não em um grupo).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Indica que o destinatário foi especificamente nomeado como um destinatário de "cc" (não em um grupo).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Indica que o destinatário foi especificamente nomeado como um "para," "cc" ou "Cco" destinatário (não em um grupo).  <br/> |
   
Provedores que não possuírem nenhum mapeamentos aparentes podem definir o grupo **PR_SENT_REPRESENTING** das propriedades para os mesmos valores que o grupo **PR_SENDER** , o grupo **PR_RCVD_REPRESENTING** das propriedades para os mesmos valores que o **PR_RECEIVED_BY **grupo e pode criar o grupo **PR_REPLY_RECIPIENT** de propriedades com base nos valores do grupo **PR_SENDER** . Por exemplo, **PR_SENT_REPRESENTING_NAME** pode ser definido como o mesmo valor que **PR_SENDER_NAME**.
  
A propriedade **PR_ENTRYID** ou **PR_ENTRYLIST** pode ser gerada, se necessário, chamando o método [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . O grupo **PR_SEARCH_KEY** das propriedades pode ser gerado concatenando a propriedade **PR_ADDRTYPE** associada a um usuário, dois-pontos (:) e a propriedade **PR_EMAIL_ADDRESS** associada ao usuário, e em seguida, alterando o resultado em maiusculas . A função de API do Windows **CharUpperBuff** é uma função conveniente usar para essa finalidade. O que é necessário desse processo é tornar uma forma canônica do endereço que pode ser comparado como uma quantidade binária. Observe que isso não é necessário se o provedor de transporte diferencia maiusculas de minúsculas com relação a endereços de email. 
  

