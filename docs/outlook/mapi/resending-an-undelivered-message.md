---
title: Reenviar uma mensagem de falha na entrega
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4fd0bf5a542e006ec743dbb7fe03d3331875c6d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770246"
---
# <a name="resending-an-undelivered-message"></a>Reenviar uma mensagem de falha na entrega
  
**Aplica-se a**: Outlook 
  
Um provedor de transporte envia um relatório de falha na entrega (NDR) quando ele não pode entregar com êxito uma mensagem enviada. É até o cliente ou não, os usuários podem tentar reenviar essas mensagens não entregues. Caso você ofereça suporte reenviar mensagens, você pode usar um formulário fornecido pelo MAPI ou implementar seus próprios. O formulário MAPI exibe os nomes dos destinatários com falha e o motivo da falha de entrega, se possível e inclui um botão que, quando selecionada, permite que um usuário reenviar a mensagem.
  
Quando uma mensagem resent é recebida, ele deve se parecer exatamente com a mensagem original. O destinatário deve ser capaz de diferenciar entre uma mensagem que foi entregue em sua primeira tentativa de transmissão ou uma tentativa de subsequente. Respostas nesta mensagem devem funcionar exatamente como se a mensagem tivesse sido enviada com êxito na primeira vez.
  
### <a name="to-resend-an-undelivered-message"></a>Para reenviar uma mensagem de falha na entrega
  
1. Chame [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para criar uma nova mensagem. 
    
2. Copiar todas as propriedades da mensagem original, excluindo o * * PR_MESSAGE_RECIPIENTS * * propriedade ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) e as propriedades **PR_SENDER** e **PR_SENT_REPRESENTING** . Faça as modificações de propriedade a seguir: 
    
   - Defina **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) para o relatório * * PR_ORIG_MESSAGE_CLASS * * propriedade ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).
    
   - Defina o sinalizador MSGFLAG_RESEND na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - Defina **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) à propriedade de **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem original.
    
   - Para cada destinatário, defina MAPI_SUBMITTED na propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Duplica cada destinatário com falha. Altere a propriedade **PR_RECIPIENT_TYPE** para o destinatário duplicado para MAPI_P1. Portanto, para cada destinatário com falha agora há duas entradas na tabela de destinatário: uma com **PR_RECIPIENT_TYPE** definido para seu valor original e a outra com **PR_RECIPIENT_TYPE** definido como MAPI_P1. 
    
3. Chame [ScCreateConversationIndex](sccreateconversationindex.md) para configurar a conversa para acompanhamento se desejado. 
    
4. Chame o método de [IMessage::ModifyRecipients](imessage-modifyrecipients.md) da nova mensagem para atualizar a lista de destinatários. 
    
5. Chame [IMessage::SubmitMessage](imessage-submitmessage.md) para salvar e enviar a mensagem nova. 
    

