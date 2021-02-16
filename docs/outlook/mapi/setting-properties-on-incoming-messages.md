---
title: Definindo propriedades em mensagens de entrada
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d7043004799d534f11aa98770e2e323cbdae95a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432692"
---
# <a name="setting-properties-on-incoming-messages"></a>Definindo propriedades em mensagens de entrada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente dentro do subsistema MAPI esperam um número de propriedades em qualquer mensagem recebida. Quando o provedor de transporte traz uma mensagem para o MAPI, ele deve definir essas propriedades, pois é o único processo com as informações necessárias para fazer isso ou é pelo menos a melhor fonte das informações.
  
Os provedores são incentivados a definir os valores de todas essas propriedades em mensagens de entrada.
  
|**Nome da propriedade**|**Descrição**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |O assunto da mensagem.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Texto de mensagem de texto sem texto simples.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Texto da mensagem RTF compactada.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |A data e a hora em que a mensagem foi entregue.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |O nome de exibição do originador da mensagem.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |A entrada do livro de endereços do originador da mensagem.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |A chave de pesquisa do livro de endereços do originador da mensagem.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |A hora em que a mensagem foi enviada ao seu sistema de mensagens pelo cliente de mensagens do remetente.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |O nome do representante representante para envio.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |A entrada do livro de endereços do representante remetente.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |A chave de pesquisa do livro de endereços do representante remetente.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |O nome do representante para recebimento.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |A entrada do livro de endereços do representante receptor.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |A chave de pesquisa do livro de endereços do representante receptor.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |A lista de nomes de exibição de destinatários delegados, separados por ponto-e-vírgula e espaço ("; ").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |A lista de destinatários delegados para uma resposta.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Indica que o destinatário foi especificamente nomeado como um destinatário "para" (não em um grupo).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Indica que o destinatário foi especificamente nomeado como um destinatário "cc" (não em um grupo).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Indica que o destinatário foi especificamente nomeado como um destinatário "para", "cc" ou "Cc" (não em um grupo).  <br/> |
   
Provedores sem mapeamentos aparentes  podem definir o grupo PR_SENT_REPRESENTING de propriedades com os mesmos valores que o grupo **PR_SENDER,** o grupo de propriedades **PR_RCVD_REPRESENTING** com os mesmos valores que o grupo **PR_RECEIVED_BY** e podem criar o grupo **PR_REPLY_RECIPIENT** de propriedades com base nos valores do grupo **PR_SENDER.** Por exemplo, **PR_SENT_REPRESENTING_NAME** pode ser definido com o mesmo valor que **PR_SENDER_NAME**.
  
A **PR_ENTRYID** ou **PR_ENTRYLIST** propriedade pode ser gerada, se necessário, chamando o método [IMAPISupport::CreateOneOff.](imapisupport-createoneoff.md) O **PR_SEARCH_KEY** grupo de propriedades pode ser gerado concatenando a propriedade PR_ADDRTYPE associada **a** um usuário, dois-pontos (:) e a propriedade PR_EMAIL_ADDRESS associada **ao** usuário) e alterando o resultado para maiúsculas. A função **charupperBuff** da API do Windows é uma função conveniente para usar para essa finalidade. O que é necessário desse processo é fazer uma forma canônica do endereço que pode ser comparado como uma quantidade binária. Observe que isso não será necessário se o provedor de transporte for sensível a caso em relação a endereços de email. 
  

