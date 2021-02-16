---
title: Abrir texto da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407533"
---
# <a name="opening-message-text"></a><span data-ttu-id="b6499-103">Abrir texto da mensagem</span><span class="sxs-lookup"><span data-stu-id="b6499-103">Opening message text</span></span>

<span data-ttu-id="b6499-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6499-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6499-105">O texto de uma mensagem é armazenado em sua **propriedade PR \_ BODY** ou **PR \_ RTF \_ COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="b6499-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="b6499-106">Para obter mais informações, consulte **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) e **PR \_ RTF \_ COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b6499-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="b6499-107">Se você tiver suporte para Rich Text Format (RTF), abra **o formato PR \_ RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="b6499-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="b6499-108">Se você não tiver suporte para RTF, abra **PR \_ BODY**.</span><span class="sxs-lookup"><span data-stu-id="b6499-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="b6499-109">Como o texto de uma mensagem pode ser grande independentemente de estar ou não formatado, use **IMAPIProp::OpenProperty** para abrir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b6499-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="b6499-110">Para obter mais informações, [consulte IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="b6499-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="b6499-111">Para exibir texto de mensagem formatado</span><span class="sxs-lookup"><span data-stu-id="b6499-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="b6499-112">Se você estiver usando um repositório de mensagens que não reconhece RTF, conforme indicado pela ausência do sinalizador STORE_RTF_OK na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do repositório:</span><span class="sxs-lookup"><span data-stu-id="b6499-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="b6499-113">Chame o método **IMAPIProp::GetProps** da mensagem para recuperar a **PR_RTF_IN_SYNC** propriedade.</span><span class="sxs-lookup"><span data-stu-id="b6499-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="b6499-114">Para obter mais informações, consulte [IMAPIProp::GetProps](imapiprop-getprops.md) e **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b6499-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="b6499-115">Chame RTFSync para sincronizar a propriedade PR_BODY mensagem com a **PR_RTF_COMPRESSED** propriedade.</span><span class="sxs-lookup"><span data-stu-id="b6499-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="b6499-116">Para obter mais informações, [consulte RTFSync,](rtfsync.md) **PR_BODY** e **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="b6499-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="b6499-117">Passe o RTF_SYNC_BODY_CHANGED sinalizador se a chamada para recuperar PR_RTF_IN_SYNC **falhou** porque a propriedade não existe ou está definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="b6499-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="b6499-118">Se **RTFSync** retornou TRUE indicando que as alterações foram feitas, chame o método **IMAPIProp::SaveChanges** da mensagem para armazená-las permanentemente.</span><span class="sxs-lookup"><span data-stu-id="b6499-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="b6499-119">Para obter mais informações, [consulte IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="b6499-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="b6499-120">Independentemente de você estar ou não usando um armazenamento de mensagens com conhecimento RTF:</span><span class="sxs-lookup"><span data-stu-id="b6499-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="b6499-121">Chame **IMAPIProp::OpenProperty** para abrir **a** PR_RTF_COMPRESSED propriedade.</span><span class="sxs-lookup"><span data-stu-id="b6499-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="b6499-122">Para obter mais informações, [consulte IMAPIProp::OpenProperty](imapiprop-openproperty.md) e **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="b6499-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="b6499-123">Se **PR_RTF_COMPRESSED** não estiver disponível, chame **OpenProperty** para abrir a **PR_BODY** propriedade.</span><span class="sxs-lookup"><span data-stu-id="b6499-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="b6499-124">Chame a **função WrapCompressedRTFStream** para criar uma versão descompactada dos dados RTF compactados, se disponível.</span><span class="sxs-lookup"><span data-stu-id="b6499-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="b6499-125">Para obter mais informações, [consulte WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="b6499-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="b6499-126">Copie o texto formatado do fluxo para o local apropriado no formulário de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b6499-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="b6499-127">Para exibir texto de mensagem simples</span><span class="sxs-lookup"><span data-stu-id="b6499-127">To display plain message text</span></span>
  
1. <span data-ttu-id="b6499-128">Chame o método **IMAPIProp::GetProps** da mensagem para recuperar a **PR_BODY** propriedade.</span><span class="sxs-lookup"><span data-stu-id="b6499-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="b6499-129">Para obter mais informações, [consulte IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="b6499-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="b6499-130">Se **GetProps** retornar PT_ERROR para o tipo de propriedade na estrutura de valores da propriedade ou MAPI_E_NOT_ENOUGH_MEMORY, chame o método **IMAPIProp::OpenProperty** da mensagem.</span><span class="sxs-lookup"><span data-stu-id="b6499-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="b6499-131">Passe **PR_BODY** como a marca de propriedade e IID_IStream como o identificador da interface.</span><span class="sxs-lookup"><span data-stu-id="b6499-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="b6499-132">Para obter mais informações, [consulte IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="b6499-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="b6499-133">Copie o texto simples do fluxo para o local apropriado no formulário de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b6499-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

