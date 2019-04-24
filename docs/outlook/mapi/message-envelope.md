---
title: Envelope de mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356921"
---
# <a name="message-envelope"></a>Envelope de mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os cabeçalhos RFC 822 são mapeados para as propriedades MAPI da seguinte maneira. PR_SENDER_\* é uma abreviação de cinco propriedades a seguir:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Abreviaturas semelhantes são usadas para PR_SENT_REPRESENTING_\* e outros grupos de propriedades de mensagem.
  
|**Cabeçalho SMTP**|**Propriedade MAPI**|
|:-----|:-----|
|De:  <br/> |Saída: PR_SENDER_\*; entrada: PR_SENDER_\* e PR_SENT_REPRESENTING_\*  <br/> |
|Pós-datados  <br/> |Saída: hora atual; entrada: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|Para:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) para destinatários onde **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) é MAPI_TO  <br/> |
|Colocado  <br/> |**PR_DISPLAY_NAME** e **PR_EMAIL_ADDRESS** para destinatários onde **PR_RECIPIENT_TYPE** é MAPI_CC  <br/> |
|Cco  <br/> |**PR_DISPLAY_NAME** e **PR_EMAIL_ADDRESS** para destinatários onde **PR_RECIPIENT_TYPE** é MAPI_BCC  <br/> |
|||
|Recebido  <br/> |Nenhuma propriedade MAPI correspondente; Coloque o nome do host local e o nome do componente aqui  <br/> |
|Return-recibo-to:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) e **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Responder para:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) e **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Assunto:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Nenhuma limitação de tamanho específica.  <br/> |
|MIME-versão:  <br/> |Sempre "1,0"  <br/> |
|||
|X-MS-Attachment:  <br/> |Para compatibilidade com o gateway SMTP do MS mail. _filename Tamanho mm-dd-yyy hh: mm_Details abaixo.  <br/> |
|||
| _envelope de mensagem SMTP inteiro_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|nome do cabeçalho TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for somente remetente. _The TBDheader deve ser usado para determinar se o remetente é capaz de interpretar o conteúdo TNEF em uma resposta.  <br/> |
|MessageId  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |Text/plain ou multipart/mixed. Consulte a seção "conteúdo da mensagem".  <br/> |
   
O cabeçalho X-MS-Attachment é formatado como quatro tokens, separados por um espaço:
  
 _tamanho do nome data hora_
  
O primeiro token é o nome de arquivo, que pode conter espaços incorporados, portanto, esse cabeçalho deve ser analisado do lado direito das mensagens de entrada. O tamanho é em bytes; a data é formatada como _mm-dd-yyyy_ e a hora como _hh: mm._
  
> [!NOTE]
> MessageID não é mapeado para **PR_SEARCH_KEY** porque o domínio SMTP tem requisitos específicos no formato do identificador da mensagem que torna impossível codificar um identificador de mensagem MAPI arbitrário. Em vez disso, MessageID é mapeado para **PR_TNEF_CORRELATION_KEY**. Esta propriedade é uma propriedade definida pelo transporte que é definida pelo transporte enviando uma mensagem de saída e usada por um transporte recebendo uma mensagem de entrada. Para obter mais informações, consulte [desenvolvimento de um provedor de transporte habilitado para TNEF](developing-a-tnef-enabled-transport-provider.md). 
  

