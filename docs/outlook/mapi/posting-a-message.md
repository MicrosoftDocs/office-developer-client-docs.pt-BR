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
ms.openlocfilehash: 61e1039a89f47fe29f9b5a1ba9203cfc88d9797e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577517"
---
# <a name="posting-a-message"></a>Postar uma mensagem

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Postar uma mensagem é semelhante ao enviar uma mensagem. A principal diferença é o destino. Em vez de serem direcionadas para um ou mais destinatários em um ou mais sistemas de mensagens, uma mensagem postada permanece em uma pasta no repositório de mensagem atual.
  
### <a name="to-post-a-message"></a>Postar uma mensagem
  
1. Abra a pasta de destino chamando [IMsgStore::OpenEntry](imsgstore-openentry.md). Se a pasta de destino for uma caixa de entrada, localize o identificador de entrada a serem passados para **OpenEntry** chamando [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Chame [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para criar a mensagem. 
    
3. Chame o método de [IMAPIProp::SetProps](imapiprop-setprops.md) da mensagem para definir: 
    
   - O sinalizador MSGFLAG_READ na propriedade **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - As propriedades **PR_SENDER** . 
    
   - As propriedades **PR_SENT_REPRESENTING** . 
    
   - A propriedade **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - A propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).
    
   - A propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - A propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Todas as propriedades necessárias para a classe da mensagem.
    
4. Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem para salvar a mensagem. 
    
5. Se necessário, crie um anexo, defina suas propriedades e salvá-lo. Para obter mais informações sobre como adicionar anexos de mensagens, consulte [Criando um anexo da mensagem](creating-a-message-attachment.md).
    
6. Chame **IMessage::SaveChanges** para salvar a mensagem. Neste ponto, ele aparecerá na tabela de conteúdo da pasta de destino. 
    
Observe que você não crie uma lista de destinatários. Em vez disso, você pode definir várias propriedades que são normalmente definidas por um provedor de transporte para uma mensagem enviada. 
  
Se você deseja salvar uma mensagem de forma intermitente antes de ter que ele apareça no índice de conteúdo da pasta visível, criá-lo em vez disso, em uma pasta oculta como a pasta raiz da subárvore IPM e depois movê-lo para a pasta de destino. 
  

