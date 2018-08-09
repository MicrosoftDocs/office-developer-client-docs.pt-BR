---
title: Postar uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 33bf6780979ee25739abf93d89744e1517363c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770184"
---
# <a name="posting-a-message"></a><span data-ttu-id="d7a30-103">Postar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="d7a30-103">Posting a message</span></span>

<span data-ttu-id="d7a30-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7a30-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7a30-105">Postar uma mensagem é semelhante ao enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7a30-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="d7a30-106">A principal diferença é o destino.</span><span class="sxs-lookup"><span data-stu-id="d7a30-106">The main difference is the destination.</span></span> <span data-ttu-id="d7a30-107">Em vez de serem direcionadas para um ou mais destinatários em um ou mais sistemas de mensagens, uma mensagem postada permanece em uma pasta no repositório de mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="d7a30-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="d7a30-108">Postar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="d7a30-108">To post a message</span></span>
  
1. <span data-ttu-id="d7a30-109">Abra a pasta de destino chamando [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d7a30-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="d7a30-110">Se a pasta de destino for uma caixa de entrada, localize o identificador de entrada a serem passados para **OpenEntry** chamando [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="d7a30-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="d7a30-111">Chame [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para criar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7a30-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="d7a30-112">Chame o método de [IMAPIProp::SetProps](imapiprop-setprops.md) da mensagem para definir:</span><span class="sxs-lookup"><span data-stu-id="d7a30-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="d7a30-113">O sinalizador MSGFLAG_READ na propriedade **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7a30-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d7a30-114">As propriedades **PR_SENDER** .</span><span class="sxs-lookup"><span data-stu-id="d7a30-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="d7a30-115">As propriedades **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="d7a30-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="d7a30-116">A propriedade **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7a30-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d7a30-117">A propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7a30-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d7a30-118">A propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7a30-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d7a30-119">A propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7a30-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="d7a30-120">Todas as propriedades necessárias para a classe da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7a30-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="d7a30-121">Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7a30-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="d7a30-122">Se necessário, crie um anexo, defina suas propriedades e salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="d7a30-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="d7a30-123">Para obter mais informações sobre como adicionar anexos de mensagens, consulte [Criando um anexo da mensagem](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="d7a30-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="d7a30-124">Chame **IMessage::SaveChanges** para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7a30-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="d7a30-125">Neste ponto, ele aparecerá na tabela de conteúdo da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="d7a30-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="d7a30-126">Observe que você não crie uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="d7a30-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="d7a30-127">Em vez disso, você pode definir várias propriedades que são normalmente definidas por um provedor de transporte para uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="d7a30-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="d7a30-128">Se você deseja salvar uma mensagem de forma intermitente antes de ter que ele apareça no índice de conteúdo da pasta visível, criá-lo em vez disso, em uma pasta oculta como a pasta raiz da subárvore IPM e depois movê-lo para a pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="d7a30-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  
