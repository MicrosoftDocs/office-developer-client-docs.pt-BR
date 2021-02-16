---
title: Criar texto da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428001"
---
# <a name="creating-message-text"></a><span data-ttu-id="60fa2-103">Criar texto da mensagem</span><span class="sxs-lookup"><span data-stu-id="60fa2-103">Creating message text</span></span>

<span data-ttu-id="60fa2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60fa2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60fa2-105">Embora algumas mensagens sejam feitas de nada mais do que uma lista de destinatários e uma linha de assunto, o conteúdo da maioria das mensagens, especificamente IPM. Anotações de mensagens, inclui texto.</span><span class="sxs-lookup"><span data-stu-id="60fa2-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="60fa2-106">O texto da mensagem pode ser simples ou formatado e armazenado em três propriedades: **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) e **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="60fa2-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="60fa2-107">Se seu cliente for baseado em texto sem texto, de definida **PR \_ BODY**.</span><span class="sxs-lookup"><span data-stu-id="60fa2-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="60fa2-108">Se você tiver suporte para texto formatado no  Formato Rich Text  (RTF), de definida PR_RTF_COMPRESSED somente ou PR_RTF_COMPRESSED e **\_ PR BODY**, dependendo do provedor de armazenamento de mensagens que você estiver usando.</span><span class="sxs-lookup"><span data-stu-id="60fa2-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="60fa2-109">Quando um cliente que reconhece RTF está usando um armazenamento de mensagens com conhecimento RTF, ele **define** PR_RTF_COMPRESSED somente.</span><span class="sxs-lookup"><span data-stu-id="60fa2-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="60fa2-110">Quando um cliente que reconhece RTF está usando um armazenamento de mensagens que não reconhece RTF, ele define ambas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="60fa2-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="60fa2-111">Se o cliente for compatível com HTML, de definida **PR_HTML** propriedade.</span><span class="sxs-lookup"><span data-stu-id="60fa2-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="60fa2-112">Determinar se o armazenamento de mensagens é compatível com o Formato Rich Text</span><span class="sxs-lookup"><span data-stu-id="60fa2-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="60fa2-113">Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do repositório de mensagens para recuperar a **propriedade PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="60fa2-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="60fa2-114">Verifique o STORE_RTF_OK bit.</span><span class="sxs-lookup"><span data-stu-id="60fa2-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="60fa2-115">Se STORE_RTF_OK for definido, o provedor de armazenamento de mensagens será compatível com texto RTF.</span><span class="sxs-lookup"><span data-stu-id="60fa2-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="60fa2-116">Se não estiver definido, o provedor do armazenamento de mensagens oferece suporte somente a texto sem texto.</span><span class="sxs-lookup"><span data-stu-id="60fa2-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="60fa2-117">Determinar se o armazenamento de mensagens é compatível com HTML</span><span class="sxs-lookup"><span data-stu-id="60fa2-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="60fa2-118">Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a **PR_STORE_SUPPORT_MASK** propriedade.</span><span class="sxs-lookup"><span data-stu-id="60fa2-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="60fa2-119">Verifique o STORE_HTML_OK bit.</span><span class="sxs-lookup"><span data-stu-id="60fa2-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="60fa2-120">Se STORE_HTML_OK for definido, o provedor de armazenamento de mensagens será compatível com texto HTML.</span><span class="sxs-lookup"><span data-stu-id="60fa2-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-pr_rtf_compressed"></a><span data-ttu-id="60fa2-121">Definir configurações de \_ RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="60fa2-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="60fa2-122">Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) da mensagem para abrir a propriedade **PR_RTF_COMPRESSED,** especificando IID_IStream como o identificador da interface e definindo o sinalizador MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="60fa2-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="60fa2-123">Chame a [função WrapCompressedRTFStream,](wrapcompressedrtfstream.md) passando o sinalizador STORE_UNCOMPRESSED_RTF se o bit STORE_UNCOMPRESSED_RTF estiver definido na propriedade PR_STORE_SUPPORT_MASK do armazenamento **de** mensagens.</span><span class="sxs-lookup"><span data-stu-id="60fa2-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="60fa2-124">Libere o fluxo original chamando seu método \*\* IUnknown::Release \*\*.</span><span class="sxs-lookup"><span data-stu-id="60fa2-124">Release the original stream by calling its \*\* IUnknown::Release \*\* method.</span></span> 
    
4. <span data-ttu-id="60fa2-125">Chame \*\* IStream::Write \*\* ou **IStream::CopyTo** para gravar o texto da mensagem no fluxo retornado de **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="60fa2-125">Call either \*\* IStream::Write \*\* or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="60fa2-126">Chame os **métodos Commit** e **Release** no fluxo retornado do **método OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="60fa2-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="60fa2-127">Neste ponto, se o provedor de armazenamento de mensagens suportar RTF, você fez tudo o que é necessário.</span><span class="sxs-lookup"><span data-stu-id="60fa2-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="60fa2-128">Você pode depender do provedor do armazenamento de mensagens para lidar com a sincronização do conteúdo e a formatação da mensagem e para criar a **propriedade PR \_ BODY,** se necessário.</span><span class="sxs-lookup"><span data-stu-id="60fa2-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="60fa2-129">Os armazenamentos de mensagens com conhecimento RTF chamam [RTFSync](rtfsync.md) para manipular a sincronização.</span><span class="sxs-lookup"><span data-stu-id="60fa2-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="60fa2-130">Se o sinalizador SYNC_BODY_CHANGED RTF estiver definido como TRUE, o provedor \_ recompute a **PR_BODY** propriedade.</span><span class="sxs-lookup"><span data-stu-id="60fa2-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="60fa2-131">Se seu provedor de armazenamento de mensagens não suporta RTF, você também deve adicionar conteúdo de mensagem não RTF definindo a **PR_BODY** propriedade.</span><span class="sxs-lookup"><span data-stu-id="60fa2-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-pr_html"></a><span data-ttu-id="60fa2-132">Definir PR_HTML</span><span class="sxs-lookup"><span data-stu-id="60fa2-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="60fa2-133">Chame o [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_HTML** com a interface **IStream.**</span><span class="sxs-lookup"><span data-stu-id="60fa2-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="60fa2-134">Chame **IStream::Write** para gravar os dados de texto da mensagem no fluxo retornado de **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="60fa2-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="60fa2-135">Chame **IStream::Commit** e **IUnknown::Release** no fluxo para confirma as alterações e liberar sua memória.</span><span class="sxs-lookup"><span data-stu-id="60fa2-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-pr_body"></a><span data-ttu-id="60fa2-136">Definir PR_BODY</span><span class="sxs-lookup"><span data-stu-id="60fa2-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="60fa2-137">Chame o [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir a propriedade **PR_BODY** com a interface **IStream.**</span><span class="sxs-lookup"><span data-stu-id="60fa2-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="60fa2-138">Chame **IStream::Write** para gravar os dados de texto da mensagem no fluxo retornado de **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="60fa2-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="60fa2-139">Chame a [função RTFSync](rtfsync.md) para sincronizar o texto com a formatação.</span><span class="sxs-lookup"><span data-stu-id="60fa2-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="60fa2-140">Como esta é uma nova mensagem, de definir os sinalizadores RTF_SYNC_RTF_CHANGED e RTF_SYNC_BODY_CHANGED para indicar que a versão RTF e a versão de texto sem alterações do texto da mensagem foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="60fa2-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="60fa2-141">**O RTFSync** definirá várias propriedades relacionadas que o provedor de armazenamento de mensagens exige, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), e as gravará na mensagem.</span><span class="sxs-lookup"><span data-stu-id="60fa2-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="60fa2-142">Chame **IStream::Commit** e **IUnknown::Release** no fluxo para confirma as alterações e liberar sua memória.</span><span class="sxs-lookup"><span data-stu-id="60fa2-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

