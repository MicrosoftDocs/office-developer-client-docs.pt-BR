---
title: Envelope da mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427189"
---
# <a name="message-envelope"></a>Envelope da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os headers RFC 822 são mapeados para propriedades MAPI da seguinte forma. PR_SENDER_ é \* uma abreviação das cinco propriedades a seguir:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Abreviaturas semelhantes são usadas para PR_SENT_REPRESENTING_ \* e outros grupos de propriedades de mensagem.
  
|**Header SMTP**|**Propriedade MAPI**|
|:-----|:-----|
|De:  <br/> |Saída: PR_SENDER_ \* ; entrada: PR_SENDER_ e \* PR_SENT_REPRESENTING_\*  <br/> |
|Data:  <br/> |Saída: hora atual; entrada: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|Para:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) para destinatários em que **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) é MAPI_TO  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME** e **PR_EMAIL_ADDRESS** para destinatários **PR_RECIPIENT_TYPE** é MAPI_CC  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME** e **PR_EMAIL_ADDRESS** para destinatários **PR_RECIPIENT_TYPE** é MAPI_BCC  <br/> |
|||
|Recebido:  <br/> |Nenhuma propriedade MAPI correspondente; colocar o nome do host local e o nome do componente aqui  <br/> |
|Retornar recibo para:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) e **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Responder:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) e **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Assunto:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Nenhuma limitação de comprimento específica.  <br/> |
|Versão MIME:  <br/> |Sempre "1.0"  <br/> |
|||
|X-MS-Attachment:  <br/> |Para compatibilidade com o gateway SMTP do MS Mail. _filename tamanho mm-dd-yyy hh:mm_Details abaixo.  <br/> |
|||
| _envelope de mensagem SMTP inteiro_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|header name TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for sender only._The TBDheader deve ser usado para determinar se o remetente é capaz de interpretar o conteúdo TNEF em uma resposta.  <br/> |
|MessageID:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |Texto/simples ou com várias partes/misto. Consulte a seção "Conteúdo da Mensagem".  <br/> |
   
O título X-MS-Attachment é formatado como quatro tokens, separados por um espaço:
  
 _name size date time_
  
O primeiro token é o nome do arquivo, que pode conter espaços incorporados, portanto, esse título deve ser analisado a partir da direita em mensagens de entrada. O tamanho é em bytes; a data é formatada  _como mm-dd-aaaa e_ a hora  _como hh:mm._
  
> [!NOTE]
> MessageID não é  mapeado para PR_SEARCH_KEY porque o domínio SMTP tem requisitos específicos no formato do identificador de mensagem que torna impossível codificar um identificador de mensagem MAPI arbitrário. Em vez disso, MessageID é mapeado **para PR_TNEF_CORRELATION_KEY**. Essa propriedade é uma propriedade definida por transporte definida pelo transporte que envia uma mensagem de saída e usada por um transporte que recebe uma mensagem de entrada. Para obter mais informações, consulte [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md). 
  

