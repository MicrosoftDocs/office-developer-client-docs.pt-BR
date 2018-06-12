---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: f6afa890f61bb2f394e3cf69e0f2c54699a2ad9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770293"
---
# <a name="rtfsync"></a><span data-ttu-id="02a90-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="02a90-103">RTFSync</span></span>

<span data-ttu-id="02a90-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02a90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02a90-105">Certifica-se de que o texto da mensagem de Rich Text Format (RTF) corresponda à versão de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="02a90-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="02a90-106">É necessário chamar essa função antes de ler a versão RTF e depois de modificar a versão RTF.</span><span class="sxs-lookup"><span data-stu-id="02a90-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02a90-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="02a90-107">Header file:</span></span>  <br/> |<span data-ttu-id="02a90-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="02a90-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="02a90-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="02a90-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="02a90-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="02a90-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="02a90-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="02a90-111">Called by:</span></span>  <br/> |<span data-ttu-id="02a90-112">Provedores de armazenamento de mensagem e aplicativos cliente com reconhecimento de RTF</span><span class="sxs-lookup"><span data-stu-id="02a90-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="02a90-113">Par�metros</span><span class="sxs-lookup"><span data-stu-id="02a90-113">Parameters</span></span>

<span data-ttu-id="02a90-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="02a90-114">_lpMessage_</span></span>
  
> <span data-ttu-id="02a90-115">[in] Ponteiro para a mensagem a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="02a90-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="02a90-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="02a90-116">_ulFlags_</span></span>
  
> <span data-ttu-id="02a90-117">[in] Bitmask dos sinalizadores usados para indicar o RTF ou a versão de texto sem formatação da mensagem foi alterada.</span><span class="sxs-lookup"><span data-stu-id="02a90-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="02a90-118">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="02a90-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="02a90-119">RTF_SYNC_BODY_CHANGED: A versão de texto sem formatação da mensagem foi alterada.</span><span class="sxs-lookup"><span data-stu-id="02a90-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="02a90-120">RTF_SYNC_RTF_CHANGED: A versão RTF da mensagem foi alterada.</span><span class="sxs-lookup"><span data-stu-id="02a90-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="02a90-121">Todos os outros bits no parâmetro _ulFlags_ são reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="02a90-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="02a90-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="02a90-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="02a90-123">[out] Ponteiro para uma variável que indica se há uma mensagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="02a90-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="02a90-124">TRUE se não houver uma mensagem atualizada, FALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="02a90-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="02a90-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="02a90-125">Return value</span></span>

<span data-ttu-id="02a90-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="02a90-126">S_OK</span></span> 
  
> <span data-ttu-id="02a90-127">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="02a90-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="02a90-128">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="02a90-128">Remarks</span></span>

<span data-ttu-id="02a90-129">Se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) está ausente ou é FALSE, antes de ler a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) a função **RTFSync** deve ser chamado com o RTF_SYNC_BODY_ ALTERADO o sinalizador definido.</span><span class="sxs-lookup"><span data-stu-id="02a90-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="02a90-130">Se o sinalizador STORE_RTF_OK não estiver definido na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), essa função deve ser chamada com o sinalizador RTF_SYNC_RTF_CHANGED definido depois de modificar **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="02a90-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="02a90-131">Se **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e o **PR_RTF_COMPRESSED** foram alterados, a função **RTFSync** deve ser chamada com os dois conjuntos de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="02a90-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="02a90-132">Se o valor do parâmetro _lpfMessageUpdated_ for definido como TRUE, o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) deve ser chamado para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="02a90-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="02a90-133">Se **SaveChanges** não for chamado, as modificações não serão salvas na mensagem.</span><span class="sxs-lookup"><span data-stu-id="02a90-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="02a90-134">Provedores de armazenamento de mensagens podem usar **RTFSync** para manter as propriedades **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="02a90-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="02a90-135">Para obter mais informações, consulte [Com suporte para texto de RTF para provedores de armazenamento de mensagem](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="02a90-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02a90-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="02a90-136">See also</span></span>

- [<span data-ttu-id="02a90-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="02a90-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

