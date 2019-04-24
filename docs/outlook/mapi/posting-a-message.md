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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350747"
---
# <a name="posting-a-message"></a><span data-ttu-id="2cd27-103">Postar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="2cd27-103">Posting a message</span></span>

<span data-ttu-id="2cd27-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cd27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cd27-105">A postagem de uma mensagem é semelhante ao envio de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="2cd27-105">Posting a message is similar to sending a message.</span></span> <span data-ttu-id="2cd27-106">A principal diferença é o destino.</span><span class="sxs-lookup"><span data-stu-id="2cd27-106">The main difference is the destination.</span></span> <span data-ttu-id="2cd27-107">Em vez de ser direcionado para um ou mais destinatários em um ou mais sistemas de mensagens, uma mensagem postada permanece em uma pasta no repositório de mensagens atual.</span><span class="sxs-lookup"><span data-stu-id="2cd27-107">Rather than being directed to one or more recipients across one or more messaging systems, a posted message remains in a folder in the current message store.</span></span>
  
### <a name="to-post-a-message"></a><span data-ttu-id="2cd27-108">Para postar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="2cd27-108">To post a message</span></span>
  
1. <span data-ttu-id="2cd27-109">Abra a pasta de destino chamando [IMsgStore:: OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="2cd27-109">Open the destination folder by calling [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="2cd27-110">Se a pasta de destino for a caixa de entrada, localize o identificador de entrada a ser passado para **OpenEntry** chamando [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="2cd27-110">If the destination folder is the Inbox, locate the entry identifier to pass to **OpenEntry** by calling [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
2. <span data-ttu-id="2cd27-111">Chame [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para criar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2cd27-111">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create the message.</span></span> 
    
3. <span data-ttu-id="2cd27-112">Chame o método [IMAPIProp::](imapiprop-setprops.md) SetProps da mensagem a ser definido:</span><span class="sxs-lookup"><span data-stu-id="2cd27-112">Call the message's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set:</span></span> 
    
   - <span data-ttu-id="2cd27-113">O sinalizador MSGFLAG_READ na propriedade **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2cd27-113">The MSGFLAG_READ flag in the **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="2cd27-114">As propriedades **PR_SENDER** .</span><span class="sxs-lookup"><span data-stu-id="2cd27-114">The **PR_SENDER** properties.</span></span> 
    
   - <span data-ttu-id="2cd27-115">As propriedades **PR_SENT_REPRESENTING** .</span><span class="sxs-lookup"><span data-stu-id="2cd27-115">The **PR_SENT_REPRESENTING** properties.</span></span> 
    
   - <span data-ttu-id="2cd27-116">A propriedade **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2cd27-116">The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="2cd27-117">A propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2cd27-117">The **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="2cd27-118">A propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2cd27-118">The **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="2cd27-119">A propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2cd27-119">The **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="2cd27-120">Todas as propriedades exigidas pela classe Message.</span><span class="sxs-lookup"><span data-stu-id="2cd27-120">Any properties required by the message class.</span></span>
    
4. <span data-ttu-id="2cd27-121">Chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2cd27-121">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the message.</span></span> 
    
5. <span data-ttu-id="2cd27-122">Se necessário, crie um anexo, defina suas propriedades e salve-o.</span><span class="sxs-lookup"><span data-stu-id="2cd27-122">If necessary, create an attachment, set its properties, and save it.</span></span> <span data-ttu-id="2cd27-123">Para obter mais informações sobre como adicionar anexos a mensagens, consulte [Creating a Message Attachment](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="2cd27-123">For more information about adding attachments to messages, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
6. <span data-ttu-id="2cd27-124">Chame **IMessage:: SaveChanges** para salvar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2cd27-124">Call **IMessage::SaveChanges** to save the message.</span></span> <span data-ttu-id="2cd27-125">Nesse ponto, ele aparecerá na tabela de conteúdo da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="2cd27-125">At this point it will appear in the contents table of the destination folder.</span></span> 
    
<span data-ttu-id="2cd27-126">Observe que você não cria uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="2cd27-126">Notice that you do not create a recipient list.</span></span> <span data-ttu-id="2cd27-127">Em vez disso, você define várias propriedades que são normalmente definidas por um provedor de transporte para uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="2cd27-127">Instead, you set several properties that are normally set by a transport provider for a sent message.</span></span> 
  
<span data-ttu-id="2cd27-128">Se você quiser salvar uma mensagem intermitentemente antes de tê-la aparecer na tabela de conteúdo da pasta visível, crie-a em vez de uma pasta oculta, como a pasta raiz da sub-árvore IPM, e mova-a para a pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="2cd27-128">If you want to save a message intermittently before having it appear in the contents table of the visible folder, create it instead in a hidden folder such as the root folder of the IPM subtree and then move it to the target folder.</span></span> 
  

