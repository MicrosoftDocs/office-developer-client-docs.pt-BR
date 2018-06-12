---
title: Encaminhamento de uma mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 146c8b4d711982118fd9da185a5b095a1bae6b2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766605"
---
# <a name="forwarding-a-message"></a>Encaminhamento de uma mensagem

**Aplica-se a**: Outlook 
  
Encaminhamento de uma mensagem envolve muitos das mesmas tarefas que enviar uma mensagem original. Primeiro, você deve abrir o armazenamento de mensagens padrão e a pasta que é designada para armazenar mensagens de saída, normalmente a caixa de saída, e chamar o método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) desta pasta para criar a mensagem para serem encaminhadas. Você também deve abrir a pasta que contém a mensagem original, normalmente a caixa de entrada. Para obter informações sobre como abrir pastas diferentes, consulte [abrindo uma pasta de repositório de mensagem](opening-a-message-store-folder.md).
  
A principal diferença entre criando uma mensagem para serem encaminhadas e criando original é que com uma mensagem encaminhada, a maioria das propriedades sejam com base em ou copiada diretamente a partir de propriedades da mensagem original. 
  
**Para encaminhar uma mensagem**
  
1. Abra o armazenamento de mensagens padrão. Para obter mais informações, consulte [abrindo o armazenamento de mensagens padrão](opening-the-default-message-store.md).
    
2. Abra a pasta caixa de saída. Para obter mais informações, consulte [Abrir uma pasta de repositório de mensagem](opening-a-message-store-folder.md).
    
3. Chame o método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) da caixa de saída para criar uma nova mensagem encaminhada. 
    
4. Chame o método de [IMAPIProp::CopyTo](imapiprop-copyto.md) da mensagem original para copiar as seguintes propriedades para a mensagem encaminhada: 
    
   - **PR\_corpo** ([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependendo se é ou não suportado Rich Text Format, HTML ou texto sem formatação.
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Copiar os anexos de mensagem da mensagem original chamando o método **IMAPIProp::CopyTo** da mensagem original para copiar a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) ou invocando o seguinte o procedimento para cada anexo a ser copiado em três etapas:
    
   1. Chame a nova encaminhadas método [IMessage::CreateAttach](imessage-createattach.md) da mensagem para criar um novo anexo. 
      
   2. Chame o método de [IMessage::OpenAttach](imessage-openattach.md) da mensagem original para abrir o anexo a ser copiado. 
      
   3. Chame o método **IMAPIProp::CopyTo** da mensagem original para copiar todas as propriedades de anexo do anexo antigo para o novo. 
    
6. Não incluem as seguintes propriedades na chamada a **IMAPIProp::CopyTo**: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |Propriedades **PR_RCVD_REPRESENTING**  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|Propriedades **PR_RECEIVED_BY**  <br/> |Propriedades **PR_REPLY_RECIPIENT**  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |Propriedades **PR_SENDER**  <br/> |
|Propriedades **PR_SENT_REPRESENTING**  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Formatar o texto da mensagem adicionando recuo e um parágrafo de cabeçalho que inclui o remetente original, data de transmissão, assunto e lista de destinatários. Não inclua caracteres de prefixo de estilo Internet com o conteúdo.
    
2. Chame [ScCreateConversationIndex](sccreateconversationindex.md), passando o valor da propriedade de **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) da mensagem original.
    
3. Defina um prefixo para a mensagem encaminhada. Se você estiver usando o padrão "firmware:", concatenar esses caracteres até o início do **PR_NORMALIZED_SUBJECT** e defina **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) para essa nova cadeia de caracteres. Não defina **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Se você estiver usando um prefixo fora do padrão, como uma cadeia de caracteres com mais de três caracteres, armazene-a em **PR_SUBJECT_PREFIX**. 
    
4. Defina as propriedades **PR_SENT_REPRESENTING** com os valores correspondentes nas propriedades do **PR_RCVD_REPRESENTING** . 
    
5. Crie uma lista de destinatários. Para obter mais informações, consulte [criar uma lista do destinatário](creating-a-recipient-list.md).
    
6. Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem encaminhada para salvá-lo ou [IMessage::SubmitMessage](imessage-submitmessage.md) para salvar e enviá-la. 
    
## <a name="see-also"></a>Confira também

- [Propriedade canônico de PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

