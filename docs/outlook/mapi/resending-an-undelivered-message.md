---
title: Reenviar uma mensagem não entregue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432664"
---
# <a name="resending-an-undelivered-message"></a>Reenviar uma mensagem não entregue
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de transporte envia uma NDR (relatório de não entrega) quando não pode entregar com êxito uma mensagem que você enviou. Fica para o cliente se os usuários podem ou não tentar reendá-las. Se você tiver suporte para reending messages, poderá usar um formulário fornecido por MAPI ou implementar o seu próprio. O formulário MAPI exibe os nomes dos destinatários com falha e o motivo da falha de entrega, se possível, e inclui um botão que, quando selecionado, permite que um usuário resende a mensagem.
  
Quando uma mensagem rente é recebida, ela deve se parecer exatamente com a mensagem original. O destinatário não deve ser capaz de diferenciar entre uma mensagem que foi entregue em sua primeira tentativa de transmissão ou uma tentativa subsequente. As respostas a essa mensagem devem funcionar exatamente como se a mensagem tivesse sido enviada com êxito na primeira vez.
  
### <a name="to-resend-an-undelivered-message"></a>Para reendar uma mensagem não entregue
  
1. Chame [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para criar uma nova mensagem. 
    
2. Copie todas as propriedades da mensagem original, excluindo a propriedade ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) e as propriedades **PR_SENDER** e **PR_SENT_REPRESENTING.** Faça as seguintes modificações de propriedade: 
    
   - De **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) para a propriedade **PR_ORIG_MESSAGE_CLASS ** do relatório ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).
    
   - Defina MSGFLAG_RESEND sinalizador na **propriedade PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - De **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) para a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem original.
    
   - Para cada destinatário, de MAPI_SUBMITTED na **propriedade PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Duplicar cada destinatário com falha. Altere **a PR_RECIPIENT_TYPE** do destinatário duplicado para MAPI_P1. Portanto, para cada destinatário com falha, agora há duas  entradas na tabela de destinatários:  uma com PR_RECIPIENT_TYPE definida como seu valor original e a outra com PR_RECIPIENT_TYPE definida como MAPI_P1. 
    
3. Chame [ScCreateConversationIndex para](sccreateconversationindex.md) configurar o rastreamento de conversa, se desejado. 
    
4. Chame o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) da nova mensagem para atualizar a lista de destinatários. 
    
5. Chame [IMessage::SubmitMessage](imessage-submitmessage.md) para salvar e enviar a nova mensagem. 
    

