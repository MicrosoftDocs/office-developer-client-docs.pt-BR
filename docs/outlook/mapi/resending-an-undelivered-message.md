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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328676"
---
# <a name="resending-an-undelivered-message"></a>Reenviar uma mensagem não entregue
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de transporte envia uma NDR (notificação de falha na entrega) quando não consegue entregar com êxito uma mensagem que você enviou. O cliente deve ou não ser capaz de tentar reenviar essas mensagens não entregues. Se você oferecer suporte à reenvio de mensagens, poderá usar um formulário fornecido por MAPI ou implementar o seu próprio. O formulário MAPI exibe os nomes dos destinatários com falha e o motivo da falha de entrega, se possível, e inclui um botão que, quando selecionado, permite que um usuário reenvie a mensagem.
  
Quando uma mensagem reenviada é recebida, ela deve ter a mesma aparência da mensagem original. O destinatário deve ser incapaz de diferenciar entre uma mensagem que foi entregue na primeira tentativa de transmissão ou uma tentativa subsequente. As respostas nesta mensagem devem funcionar exatamente como se a mensagem tivesse sido enviada com êxito pela primeira vez.
  
### <a name="to-resend-an-undelivered-message"></a>Para reenviar uma mensagem não entregue
  
1. Chame [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para criar uma nova mensagem. 
    
2. Copie todas as propriedades da mensagem original, excluindo a propriedade * * PR_MESSAGE_RECIPIENTS * * ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) e as propriedades **PR_SENDER** e **PR_SENT_REPRESENTING** . Faça as seguintes modificações de propriedade: 
    
   - Defina **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) para a propriedade * * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) do relatório.
    
   - Defina o sinalizador MSGFLAG_RESEND na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - Defina **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) para a propriedade **PR_ENTRYID** da mensagem original ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
   - Para cada destinatário, defina MAPI_SUBMITTED na propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Duplique cada destinatário com falha. Altere a propriedade **PR_RECIPIENT_TYPE** do destinatário duplicado para MAPI_P1. Portanto, para cada destinatário com falha, há agora duas entradas na tabela de destinatários: uma com **PR_RECIPIENT_TYPE** definida para seu valor original e a outra com **PR_RECIPIENT_TYPE** definido como MAPI_P1. 
    
3. Chame [ScCreateConversationIndex](sccreateconversationindex.md) para configurar o rastreamento de conversa, se desejado. 
    
4. Chame o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) da nova mensagem para atualizar a lista de destinatários. 
    
5. Chame [IMessage:: SubmitMessage](imessage-submitmessage.md) para salvar e enviar a nova mensagem. 
    

