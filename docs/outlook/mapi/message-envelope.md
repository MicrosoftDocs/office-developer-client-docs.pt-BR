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
ms.openlocfilehash: fd642575a3136eef3193e0bdbe884cf8f54ba337
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571294"
---
# <a name="message-envelope"></a>Envelope da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cabeçalhos de RFC 822 são mapeados para propriedades MAPI. PR_SENDER_\* é uma abreviação de 5 propriedades a seguir:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Semelhantes abreviações são usadas para PR_SENT_REPRESENTING_\* e outros grupos de propriedades de mensagem.
  
|**Cabeçalho de SMTP**|**Propriedade MAPI**|
|:-----|:-----|
|De:  <br/> |Saída: PR_SENDER_\*; entrada: PR_SENDER_\* e PR_SENT_REPRESENTING_\*  <br/> |
|Data:  <br/> |Saída: hora atual; entrada: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|Para:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) para destinatários onde **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) é MAPI_TO  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME** e **PR_EMAIL_ADDRESS** para destinatários onde **PR_RECIPIENT_TYPE** é MAPI_CC  <br/> |
|Cco:  <br/> |**PR_DISPLAY_NAME** e **PR_EMAIL_ADDRESS** para destinatários onde **PR_RECIPIENT_TYPE** é MAPI_BCC  <br/> |
|||
|Recebidos:  <br/> |Nenhuma propriedade MAPI correspondente; Coloque o nome de host local e o nome do componente aqui  <br/> |
|Confirmação de retorno para:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) e **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Responder para:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) e **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Assunto:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Nenhuma limitação de comprimento específico.  <br/> |
|MIME-version:  <br/> |Sempre "1.0"  <br/> |
|||
|X-MS-anexo:  <br/> |Para compatibilidade com o gateway MS email SMTP. _filename tamanho dd-mm-yyy hh:mm_Details abaixo.  <br/> |
|||
| _envelope de mensagem SMTP inteira_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|TBD de nome de cabeçalho  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for remetente somente ._The TBDheader deve ser usado para determinar se o remetente é capaz de interpretar conteúdo TNEF em uma resposta.  <br/> |
|MessageID:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |O texto/simples ou com diversas partes/resumida. Consulte a seção "Mensagem conteúdo".  <br/> |
   
O cabeçalho X-MS-anexo está formatado como tokens de quatro, separados por um espaço:
  
 _nome tamanho data/hora_
  
O primeiro token é o nome de arquivo, que pode conter espaços incorporados, portanto este cabeçalho deve ser analisado a partir de mensagens de entrada diretamente neles. O tamanho é em bytes; a data é formatada como _dd-mm-aaaa_ e a hora como _hh: mm._
  
> [!NOTE]
> MessageID não for mapeado em **PR_SEARCH_KEY** , porque o domínio SMTP tem requisitos específicos no menu Formatar do identificador de mensagem impossibilitar codificar um identificador de mensagem MAPI arbitrário. Em vez disso, MessageID é mapeado para **PR_TNEF_CORRELATION_KEY**. Essa propriedade é uma propriedade definida pelo transporte que é definida pelo transporte enviando uma mensagem de saída e usada por um transporte recebendo uma mensagem de entrada. Para obter mais informações, consulte [desenvolvendo um provedor de transporte TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  

