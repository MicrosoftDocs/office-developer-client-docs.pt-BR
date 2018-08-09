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
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="611e6-103">Reenviar uma mensagem de falha na entrega</span><span class="sxs-lookup"><span data-stu-id="611e6-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="611e6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="611e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="611e6-105">Um provedor de transporte envia um relatório de falha na entrega (NDR) quando ele não pode entregar com êxito uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="611e6-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="611e6-106">É até o cliente ou não, os usuários podem tentar reenviar essas mensagens não entregues.</span><span class="sxs-lookup"><span data-stu-id="611e6-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="611e6-107">Caso você ofereça suporte reenviar mensagens, você pode usar um formulário fornecido pelo MAPI ou implementar seus próprios.</span><span class="sxs-lookup"><span data-stu-id="611e6-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="611e6-108">O formulário MAPI exibe os nomes dos destinatários com falha e o motivo da falha de entrega, se possível e inclui um botão que, quando selecionada, permite que um usuário reenviar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="611e6-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="611e6-109">Quando uma mensagem resent é recebida, ele deve se parecer exatamente com a mensagem original.</span><span class="sxs-lookup"><span data-stu-id="611e6-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="611e6-110">O destinatário deve ser capaz de diferenciar entre uma mensagem que foi entregue em sua primeira tentativa de transmissão ou uma tentativa de subsequente.</span><span class="sxs-lookup"><span data-stu-id="611e6-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="611e6-111">Respostas nesta mensagem devem funcionar exatamente como se a mensagem tivesse sido enviada com êxito na primeira vez.</span><span class="sxs-lookup"><span data-stu-id="611e6-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="611e6-112">Para reenviar uma mensagem de falha na entrega</span><span class="sxs-lookup"><span data-stu-id="611e6-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="611e6-113">Chame [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para criar uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="611e6-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="611e6-114">Copiar todas as propriedades da mensagem original, excluindo o * * PR_MESSAGE_RECIPIENTS * * propriedade ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) e as propriedades **PR_SENDER** e **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="611e6-114">Copy all of the properties from the original message, excluding the ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="611e6-115">Faça as modificações de propriedade a seguir:</span><span class="sxs-lookup"><span data-stu-id="611e6-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="611e6-116">Defina **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) para o relatório * * PR_ORIG_MESSAGE_CLASS * * propriedade ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="611e6-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="611e6-117">Defina o sinalizador MSGFLAG_RESEND na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="611e6-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="611e6-118">Defina **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) à propriedade de **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="611e6-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="611e6-119">Para cada destinatário, defina MAPI_SUBMITTED na propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="611e6-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="611e6-120">Duplica cada destinatário com falha.</span><span class="sxs-lookup"><span data-stu-id="611e6-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="611e6-121">Altere a propriedade **PR_RECIPIENT_TYPE** para o destinatário duplicado para MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="611e6-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="611e6-122">Portanto, para cada destinatário com falha agora há duas entradas na tabela de destinatário: uma com **PR_RECIPIENT_TYPE** definido para seu valor original e a outra com **PR_RECIPIENT_TYPE** definido como MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="611e6-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="611e6-123">Chame [ScCreateConversationIndex](sccreateconversationindex.md) para configurar a conversa para acompanhamento se desejado.</span><span class="sxs-lookup"><span data-stu-id="611e6-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="611e6-124">Chame o método de [IMessage::ModifyRecipients](imessage-modifyrecipients.md) da nova mensagem para atualizar a lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="611e6-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="611e6-125">Chame [IMessage::SubmitMessage](imessage-submitmessage.md) para salvar e enviar a mensagem nova.</span><span class="sxs-lookup"><span data-stu-id="611e6-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

