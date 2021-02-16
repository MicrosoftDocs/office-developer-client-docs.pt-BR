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
  
Postar uma mensagem é semelhante ao envio de uma mensagem. A principal diferença é o destino. Em vez de ser direcionada para um ou mais destinatários em um ou mais sistemas de mensagens, uma mensagem postada permanece em uma pasta no armazenamento de mensagens atual.
  
### <a name="to-post-a-message"></a>Para postar uma mensagem
  
1. Abra a pasta de destino chamando [IMsgStore::OpenEntry](imsgstore-openentry.md). Se a pasta de destino for a Caixa de Entrada, localize o identificador de entrada a ser passado para **OpenEntry** chamando [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Chame [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para criar a mensagem. 
    
3. Chame o método [IMAPIProp::SetProps](imapiprop-setprops.md) da mensagem para definir: 
    
   - O MSGFLAG_READ sinalizador na propriedade **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - As **PR_SENDER** propriedades. 
    
   - As **PR_SENT_REPRESENTING** propriedades. 
    
   - A **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) .
    
   - A **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) **ou PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) propriedade.
    
   - A **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) .
    
   - A **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) .
    
   - Todas as propriedades exigidas pela classe message.
    
4. Chame o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem para salvar a mensagem. 
    
5. Se necessário, crie um anexo, de definir suas propriedades e salve-o. Para obter mais informações sobre como adicionar anexos a mensagens, consulte [Criando um anexo de mensagem.](creating-a-message-attachment.md)
    
6. Chame **IMessage::SaveChanges** para salvar a mensagem. Neste ponto, ele aparecerá no índice da pasta de destino. 
    
Observe que você não cria uma lista de destinatários. Em vez disso, você pode definir várias propriedades que normalmente são definidas por um provedor de transporte para uma mensagem enviada. 
  
Se você quiser salvar uma mensagem intermitentemente antes de que ela apareça no índice de conteúdo da pasta visível, crie-a em uma pasta oculta, como a pasta raiz da subárvore do IPM, e mova-a para a pasta de destino. 
  

