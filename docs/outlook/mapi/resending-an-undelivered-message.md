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
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="a62c7-103">Reenviar uma mensagem não entregue</span><span class="sxs-lookup"><span data-stu-id="a62c7-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="a62c7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a62c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a62c7-105">Um provedor de transporte envia uma NDR (notificação de falha na entrega) quando não consegue entregar com êxito uma mensagem que você enviou.</span><span class="sxs-lookup"><span data-stu-id="a62c7-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="a62c7-106">O cliente deve ou não ser capaz de tentar reenviar essas mensagens não entregues.</span><span class="sxs-lookup"><span data-stu-id="a62c7-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="a62c7-107">Se você oferecer suporte à reenvio de mensagens, poderá usar um formulário fornecido por MAPI ou implementar o seu próprio.</span><span class="sxs-lookup"><span data-stu-id="a62c7-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="a62c7-108">O formulário MAPI exibe os nomes dos destinatários com falha e o motivo da falha de entrega, se possível, e inclui um botão que, quando selecionado, permite que um usuário reenvie a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a62c7-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="a62c7-109">Quando uma mensagem reenviada é recebida, ela deve ter a mesma aparência da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="a62c7-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="a62c7-110">O destinatário deve ser incapaz de diferenciar entre uma mensagem que foi entregue na primeira tentativa de transmissão ou uma tentativa subsequente.</span><span class="sxs-lookup"><span data-stu-id="a62c7-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="a62c7-111">As respostas nesta mensagem devem funcionar exatamente como se a mensagem tivesse sido enviada com êxito pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="a62c7-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="a62c7-112">Para reenviar uma mensagem não entregue</span><span class="sxs-lookup"><span data-stu-id="a62c7-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="a62c7-113">Chame [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para criar uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="a62c7-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="a62c7-114">Copie todas as propriedades da mensagem original, excluindo a propriedade \* \* PR_MESSAGE_RECIPIENTS \* \* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) e as propriedades **PR_SENDER** e **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="a62c7-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="a62c7-115">Faça as seguintes modificações de propriedade:</span><span class="sxs-lookup"><span data-stu-id="a62c7-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="a62c7-116">Defina **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) para a propriedade \* \* PR_ORIG_MESSAGE_CLASS \* \* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) do relatório.</span><span class="sxs-lookup"><span data-stu-id="a62c7-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="a62c7-117">Defina o sinalizador MSGFLAG_RESEND na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a62c7-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="a62c7-118">Defina **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) para a propriedade **PR_ENTRYID** da mensagem original ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a62c7-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="a62c7-119">Para cada destinatário, defina MAPI_SUBMITTED na propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a62c7-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="a62c7-120">Duplique cada destinatário com falha.</span><span class="sxs-lookup"><span data-stu-id="a62c7-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="a62c7-121">Altere a propriedade **PR_RECIPIENT_TYPE** do destinatário duplicado para MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="a62c7-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="a62c7-122">Portanto, para cada destinatário com falha, há agora duas entradas na tabela de destinatários: uma com **PR_RECIPIENT_TYPE** definida para seu valor original e a outra com **PR_RECIPIENT_TYPE** definido como MAPI_P1.</span><span class="sxs-lookup"><span data-stu-id="a62c7-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="a62c7-123">Chame [ScCreateConversationIndex](sccreateconversationindex.md) para configurar o rastreamento de conversa, se desejado.</span><span class="sxs-lookup"><span data-stu-id="a62c7-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="a62c7-124">Chame o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) da nova mensagem para atualizar a lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="a62c7-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="a62c7-125">Chame [IMessage:: SubmitMessage](imessage-submitmessage.md) para salvar e enviar a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="a62c7-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

