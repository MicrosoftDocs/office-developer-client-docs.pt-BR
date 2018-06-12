---
title: Criando o texto da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 38be3bc2df8931ca45da12e43436377545e8a977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766380"
---
# <a name="creating-message-text"></a><span data-ttu-id="ea679-103">Criando o texto da mensagem</span><span class="sxs-lookup"><span data-stu-id="ea679-103">Creating message text</span></span>

<span data-ttu-id="ea679-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea679-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea679-105">Embora algumas mensagens são compostas de nada mais que uma lista de destinatários e uma linha de assunto, o conteúdo da maioria das mensagens, especificamente IPM. Observação as mensagens, inclui o texto.</span><span class="sxs-lookup"><span data-stu-id="ea679-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="ea679-106">Mensagem de texto pode ser simples ou formatada e está armazenado em três propriedades: **PR\_corpo** ([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ea679-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="ea679-107">Se seu cliente é baseado em texto sem formatação, defina **PR\_corpo**.</span><span class="sxs-lookup"><span data-stu-id="ea679-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="ea679-108">Caso você ofereça suporte texto formatado em Rich Text Format (RTF), definidos **PR_RTF_COMPRESSED** apenas ou ambos os **PR_RTF_COMPRESSED** e **PR\_corpo**, dependendo do provedor de armazenamento de mensagem que você está usando.</span><span class="sxs-lookup"><span data-stu-id="ea679-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="ea679-109">Quando um cliente RTF reconhecimento estiver usando um armazenamento de mensagens RTF reconhecimento, ela define **PR_RTF_COMPRESSED** somente.</span><span class="sxs-lookup"><span data-stu-id="ea679-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="ea679-110">Quando um cliente RTF reconhecimento estiver usando um armazenamento de mensagens sem reconhecimento de RTF, ela define ambas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="ea679-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="ea679-111">Se seu cliente ofereça suporte a HTML, defina a propriedade **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="ea679-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="ea679-112">Determinar se o seu armazenamento de mensagens suporta formato Rich Text</span><span class="sxs-lookup"><span data-stu-id="ea679-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="ea679-113">Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ea679-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="ea679-114">Verifique se o bit STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="ea679-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="ea679-115">Se STORE_RTF_OK for definido, o provedor de armazenamento de mensagem suporta texto RTF.</span><span class="sxs-lookup"><span data-stu-id="ea679-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="ea679-116">Se não estiver definida, o provedor de armazenamento de mensagem suporta apenas texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="ea679-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="ea679-117">Determinar se o seu armazenamento de mensagens oferece suporte a HTML</span><span class="sxs-lookup"><span data-stu-id="ea679-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="ea679-118">Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a propriedade **PR_STORE_SUPPORT_MASK** .</span><span class="sxs-lookup"><span data-stu-id="ea679-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="ea679-119">Verifique se o bit STORE_HTML_OK.</span><span class="sxs-lookup"><span data-stu-id="ea679-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="ea679-120">Se STORE_HTML_OK for definido, o provedor de armazenamento de mensagem suporta texto HTML.</span><span class="sxs-lookup"><span data-stu-id="ea679-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-prrtfcompressed"></a><span data-ttu-id="ea679-121">Definir PR\_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="ea679-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="ea679-122">Chame o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) da mensagem para abrir a propriedade **PR_RTF_COMPRESSED** , especificando IID_IStream como o identificador de interface e definindo o sinalizador MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="ea679-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="ea679-123">Chame a função [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , passando o sinalizador STORE_UNCOMPRESSED_RTF se o bit STORE_UNCOMPRESSED_RTF é definido na propriedade **PR_STORE_SUPPORT_MASK** do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ea679-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="ea679-124">Liberar o fluxo original chamando seu * * IUnknown:: Release * * método.</span><span class="sxs-lookup"><span data-stu-id="ea679-124">Release the original stream by calling its ** IUnknown::Release ** method.</span></span> 
    
4. <span data-ttu-id="ea679-125">Chamar tanto * * IStream::Write * * ou **IStream::CopyTo** para gravar o fluxo de texto da mensagem retornado da **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="ea679-125">Call either ** IStream::Write ** or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="ea679-126">Chame os métodos **Commit** e a **versão** no fluxo retornado pelo método **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="ea679-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="ea679-127">Neste ponto, se o provedor de armazenamento de mensagem suporta RTF, você fez tudo o que é necessário.</span><span class="sxs-lookup"><span data-stu-id="ea679-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="ea679-128">Você pode depender o provedor de armazenamento de mensagem para lidar com formatação e sincronizando conteúdo da mensagem e criar o **PR\_corpo** propriedade, se necessário.</span><span class="sxs-lookup"><span data-stu-id="ea679-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="ea679-129">Repositórios de mensagem RTF reconhecimento chame [RTFSync](rtfsync.md) para lidar com a sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea679-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="ea679-130">Se o RTF\_sinalizador SYNC_BODY_CHANGED é definido como TRUE, o provedor será recompilar a propriedade **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="ea679-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="ea679-131">Se o seu provedor de armazenamento de mensagens não oferece suporte a RTF, você também deve adicionar o conteúdo da mensagem não-RTF, definindo a propriedade **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="ea679-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-prhtml"></a><span data-ttu-id="ea679-132">Definir PR_HTML</span><span class="sxs-lookup"><span data-stu-id="ea679-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="ea679-133">Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_HTML** com a interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="ea679-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="ea679-134">Chame **IStream::Write** para gravar os dados de texto de mensagem no fluxo retornado da **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="ea679-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="ea679-135">Chamadas **IStream::Commit** e **IUnknown:: Release** no fluxo para confirmar as alterações e liberar sua memória.</span><span class="sxs-lookup"><span data-stu-id="ea679-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-prbody"></a><span data-ttu-id="ea679-136">Definir PR_BODY</span><span class="sxs-lookup"><span data-stu-id="ea679-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="ea679-137">Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_BODY** com a interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="ea679-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="ea679-138">Chame **IStream::Write** para gravar os dados de texto de mensagem no fluxo retornado da **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="ea679-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="ea679-139">Chame a função [RTFSync](rtfsync.md) para sincronizar o texto com a formatação.</span><span class="sxs-lookup"><span data-stu-id="ea679-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="ea679-140">Como esta é uma nova mensagem, defina o RTF_SYNC_RTF_CHANGED e o RTF_SYNC_BODY_CHANGED sinalizadores para indicar que a versão RTF tanto o texto sem formatação do texto da mensagem foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ea679-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="ea679-141">**RTFSync** irá definir várias propriedades relacionadas que requer que o provedor de armazenamento de mensagens, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) e gravá-los à mensagem.</span><span class="sxs-lookup"><span data-stu-id="ea679-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="ea679-142">Chamadas **IStream::Commit** e **IUnknown:: Release** no fluxo para confirmar as alterações e liberar sua memória.</span><span class="sxs-lookup"><span data-stu-id="ea679-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

