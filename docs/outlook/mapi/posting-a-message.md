---
title: Postar uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429765"
---
# <a name="posting-a-message"></a>Postar uma mensagem

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A postagem de uma mensagem é semelhante ao envio de uma mensagem. A principal diferença é o destino. Em vez de ser direcionado para um ou mais destinatários em um ou mais sistemas de mensagens, uma mensagem postada permanece em uma pasta no repositório de mensagens atual.
  
### <a name="to-post-a-message"></a>Para postar uma mensagem
  
1. Abra a pasta de destino chamando [IMsgStore:: OpenEntry](imsgstore-openentry.md). Se a pasta de destino for a caixa de entrada, localize o identificador de entrada a ser passado para **OpenEntry** chamando [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Chame [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para criar a mensagem. 
    
3. Chame o método [IMAPIProp::](imapiprop-setprops.md) SetProps da mensagem a ser definido: 
    
   - O sinalizador MSGFLAG_READ na propriedade **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - As propriedades **PR_SENDER** . 
    
   - As propriedades **PR_SENT_REPRESENTING** . 
    
   - A propriedade **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - A propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - A propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - A propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Todas as propriedades exigidas pela classe Message.
    
4. Chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem para salvar a mensagem. 
    
5. Se necessário, crie um anexo, defina suas propriedades e salve-o. Para obter mais informações sobre como adicionar anexos a mensagens, consulte [Creating a Message Attachment](creating-a-message-attachment.md).
    
6. Chame **IMessage:: SaveChanges** para salvar a mensagem. Nesse ponto, ele aparecerá na tabela de conteúdo da pasta de destino. 
    
Observe que você não cria uma lista de destinatários. Em vez disso, você define várias propriedades que são normalmente definidas por um provedor de transporte para uma mensagem enviada. 
  
Se você quiser salvar uma mensagem intermitentemente antes de tê-la aparecer na tabela de conteúdo da pasta visível, crie-a em vez de uma pasta oculta, como a pasta raiz da sub-árvore IPM, e mova-a para a pasta de destino. 
  

