---
title: Texto da mensagem de abertura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ad3499cc1ff3bd8b633fa48173ab8455d5d8d124
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768181"
---
# <a name="opening-message-text"></a><span data-ttu-id="1b6a6-103">Texto da mensagem de abertura</span><span class="sxs-lookup"><span data-stu-id="1b6a6-103">Opening message text</span></span>

<span data-ttu-id="1b6a6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b6a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b6a6-105">O texto de uma mensagem é armazenado no seu **PR\_corpo** propriedade ou **PR\_RTF\_COMPRESSED** propriedade.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="1b6a6-106">Para obter mais informações, consulte **PR\_corpo** ([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([Taghtml](pidtaghtml-canonical-property.md)) e **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1b6a6-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="1b6a6-107">Caso você ofereça suporte a Rich Text Format (RTF), abra **PR\_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="1b6a6-108">Se você não suportam RTF, abra **PR\_corpo**.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="1b6a6-109">Como o texto de uma mensagem pode ser grande, independentemente de estarem ou não está formatado, use **IMAPIProp::OpenProperty** para abrir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="1b6a6-110">Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1b6a6-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="1b6a6-111">Para exibir o texto de mensagem de formatado</span><span class="sxs-lookup"><span data-stu-id="1b6a6-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="1b6a6-112">Se você estiver usando um armazenamento de mensagens de reconhecimento de não-RTF, conforme indicado pela ausência do sinalizador STORE_RTF_OK na propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) da loja:</span><span class="sxs-lookup"><span data-stu-id="1b6a6-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="1b6a6-113">Chame o método de **IMAPIProp::GetProps** da mensagem para recuperar a propriedade **PR_RTF_IN_SYNC** .</span><span class="sxs-lookup"><span data-stu-id="1b6a6-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="1b6a6-114">Para obter mais informações, consulte [IMAPIProp::GetProps](imapiprop-getprops.md) e **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1b6a6-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="1b6a6-115">Chame RTFSync para sincronizar a propriedade PR_BODY da mensagem com a propriedade **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="1b6a6-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="1b6a6-116">Para obter mais informações, consulte [RTFSync](rtfsync.md), **PR_BODY**e **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="1b6a6-117">PASS o RTF_SYNC_BODY_CHANGED sinalizar se a chamada para recuperar **PR_RTF_IN_SYNC** falhou porque a propriedade não existe ou ela é definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="1b6a6-118">Se **RTFSync** retornado TRUE — indicando que as alterações foram feitas — chamar o método de **IMAPIProp::SaveChanges** da mensagem para permanentemente armazená-los.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="1b6a6-119">Para obter mais informações, consulte [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="1b6a6-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="1b6a6-120">Independentemente de estarem ou não estiver usando uma mensagem RTF reconhecimento armazene:</span><span class="sxs-lookup"><span data-stu-id="1b6a6-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="1b6a6-121">Chame **IMAPIProp::OpenProperty** para abrir a propriedade **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="1b6a6-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="1b6a6-122">Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="1b6a6-123">Se **PR_RTF_COMPRESSED** não estiver disponível, chame **OpenProperty** para abrir a propriedade **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="1b6a6-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="1b6a6-124">Chame a função de **WrapCompressedRTFStream** para criar uma versão descompactada dos dados compactados RTF, se disponível.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="1b6a6-125">Para obter mais informações, consulte [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="1b6a6-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="1b6a6-126">Copie o texto formatado do stream até o local apropriado no formulário da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="1b6a6-127">Para exibir texto sem formatação de mensagem</span><span class="sxs-lookup"><span data-stu-id="1b6a6-127">To display plain message text</span></span>
  
1. <span data-ttu-id="1b6a6-128">Chame o método de **IMAPIProp::GetProps** da mensagem para recuperar a propriedade **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="1b6a6-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="1b6a6-129">Para obter mais informações, consulte [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="1b6a6-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="1b6a6-130">Se **GetProps** retornar qualquer PT_ERROR o tipo de propriedade na estrutura do valor de propriedade ou MAPI_E_NOT_ENOUGH_MEMORY, chame o método de **IMAPIProp::OpenProperty** da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="1b6a6-131">Passe **PR_BODY** como a marca de propriedade e IID_IStream como o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="1b6a6-132">Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1b6a6-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="1b6a6-133">Copie o texto sem formatação do stream até o local apropriado no formulário da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    
