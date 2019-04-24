---
title: Encaminhar uma mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d1df84c37cc2a24806c35ae0c90e4bf2a5e438d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328060"
---
# <a name="forwarding-a-message"></a>Encaminhar uma mensagem

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O encaminhamento de uma mensagem envolve muitas das mesmas tarefas que o envio de uma mensagem original. Primeiro, você deve abrir o repositório de mensagens padrão e a pasta designada para manter as mensagens de saída, normalmente a de saída e chamar o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) da pasta para criar a mensagem a ser encaminhada. Você também deve abrir a pasta que contém a mensagem original, normalmente a caixa de entrada. Para obter informações sobre como abrir pastas diferentes, consulte [abrir uma pasta de armazenamento de mensagens](opening-a-message-store-folder.md).
  
A principal diferença entre a criação de uma mensagem a ser encaminhada e a criação do original é que com uma mensagem encaminhada, a maioria das propriedades é baseada ou copiada diretamente das propriedades da mensagem original. 
  
**Para encaminhar uma mensagem**
  
1. Abra o repositório de mensagens padrão. Para obter mais informações, consulte [abrindo o repositório de mensagens padrão](opening-the-default-message-store.md).
    
2. Abra a pasta de saída. Para obter mais informações, consulte [abrir uma pasta de armazenamento de mensagens](opening-a-message-store-folder.md).
    
3. Chame o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) da webquery para criar uma nova mensagem encaminhada. 
    
4. Chame o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) da mensagem original para copiar as seguintes propriedades para a mensagem encaminhada: 
    
   - **PR\_Body** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), dependendo se você tem ou não suporte para formato Rich Text, texto sem formatação ou HTML.
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Copie os anexos da mensagem original chamando o método **IMAPIProp:: CopyTo** da mensagem original para copiar a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) ou invocar o seguinte procedimento de três etapas para cada anexo a ser copiado:
    
   1. Chame o novo método [IMessage:: CreateAttach](imessage-createattach.md) da mensagem encaminhada para criar um novo anexo. 
      
   2. Chame o método [IMessage:: OpenAttach](imessage-openattach.md) da mensagem original para abrir o anexo a ser copiado. 
      
   3. Chame o método **IMAPIProp:: CopyTo** da mensagem original para copiar todas as propriedades de anexo do anexo antigo para o novo. 
    
6. Não inclua as seguintes propriedades em sua chamada para **IMAPIProp:: CopyTo**: 
    
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
   
1. Formatar o texto da mensagem adicionando recuo e um parágrafo de cabeçalho que inclui o remetente original, a data de transmissão, o assunto e a lista de destinatários. Não inclua caracteres de prefixo de estilo da Internet com o conteúdo.
    
2. Chame [ScCreateConversationIndex](sccreateconversationindex.md), passando o valor da propriedade **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) da mensagem original.
    
3. Defina um prefixo para a mensagem encaminhada. Se você estiver usando o padrão "FW:", concatene esses caracteres no início do **PR_NORMALIZED_SUBJECT** e defina **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) para essa nova cadeia de caracteres. Não defina **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Se você estiver usando um prefixo não padrão, como uma cadeia de caracteres com mais de três caracteres, armazene-o no **PR_SUBJECT_PREFIX**. 
    
4. Defina as propriedades de **PR_SENT_REPRESENTING** para os valores correspondentes nas propriedades de **PR_RCVD_REPRESENTING** . 
    
5. Criar uma lista de destinatários. Para obter mais informações, consulte [Creating a Recipient List](creating-a-recipient-list.md).
    
6. Chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem encaminhada para salvá-lo ou [IMessage:: SubmitMessage](imessage-submitmessage.md) para salvá-lo e enviá-lo. 
    
## <a name="see-also"></a>Confira também

- [Propriedade canônica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

