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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316475"
---
# <a name="rtfsync"></a><span data-ttu-id="60032-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="60032-103">RTFSync</span></span>

<span data-ttu-id="60032-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60032-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60032-105">Verifica se o texto da mensagem RTF (Rich Text Format) corresponde à versão de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="60032-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="60032-106">É necessário chamar essa função antes de ler a versão RTF e depois de modificar a versão RTF.</span><span class="sxs-lookup"><span data-stu-id="60032-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60032-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="60032-107">Header file:</span></span>  <br/> |<span data-ttu-id="60032-108">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="60032-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="60032-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="60032-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="60032-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="60032-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="60032-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="60032-111">Called by:</span></span>  <br/> |<span data-ttu-id="60032-112">Aplicativos clientes com reconhecimento de RTF e provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="60032-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="60032-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60032-113">Parameters</span></span>

<span data-ttu-id="60032-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="60032-114">_lpMessage_</span></span>
  
> <span data-ttu-id="60032-115">no Ponteiro para a mensagem a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="60032-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="60032-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="60032-116">_ulFlags_</span></span>
  
> <span data-ttu-id="60032-117">no Bitmask dos sinalizadores usados para indicar que a versão em RTF ou texto sem formatação da mensagem foi alterada.</span><span class="sxs-lookup"><span data-stu-id="60032-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="60032-118">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="60032-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="60032-119">RTF_SYNC_BODY_CHANGED: a versão de texto sem formatação da mensagem foi alterada.</span><span class="sxs-lookup"><span data-stu-id="60032-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="60032-120">RTF_SYNC_RTF_CHANGED: a versão RTF da mensagem foi alterada.</span><span class="sxs-lookup"><span data-stu-id="60032-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="60032-121">Todos os outros bits no parâmetro _parâmetroulflags_ são reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="60032-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="60032-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="60032-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="60032-123">bota Ponteiro para uma variável que indica se há uma mensagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="60032-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="60032-124">TRUE se houver uma mensagem atualizada; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="60032-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60032-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="60032-125">Return value</span></span>

<span data-ttu-id="60032-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="60032-126">S_OK</span></span> 
  
> <span data-ttu-id="60032-127">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="60032-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60032-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="60032-128">Remarks</span></span>

<span data-ttu-id="60032-129">Se a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) estiver ausente ou for false, antes de ler a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), a função **RTFSync** deverá ser chamada com o RTF_SYNC_BODY_ Conjunto de sinalizadores alterado.</span><span class="sxs-lookup"><span data-stu-id="60032-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="60032-130">Se o sinalizador STORE_RTF_OK não estiver definido na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), essa função deverá ser chamada com o sinalizador RTF_SYNC_RTF_CHANGED definido após a modificação de **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="60032-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="60032-131">Se ambos os **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e **PR_RTF_COMPRESSED** tiverem sido alterados, a função **RTFSync** deverá ser chamada com ambos os sinalizadores definidos.</span><span class="sxs-lookup"><span data-stu-id="60032-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="60032-132">Se o valor do parâmetro _lpfMessageUpdated_ for definido como true, o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) deverá ser chamado para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="60032-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="60032-133">Se **SaveChanges** não for chamado, as modificações não serão salvas na mensagem.</span><span class="sxs-lookup"><span data-stu-id="60032-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="60032-134">Os provedores de repositórios de mensagens podem usar o **RTFSync** para manter as propriedades **PR_BODY** e **PR_RTF_COMPRESSED** sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="60032-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="60032-135">Para obter mais informações, consulte [suporte a texto RTF para provedores de repositório de mensagens](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="60032-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60032-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="60032-136">See also</span></span>

- [<span data-ttu-id="60032-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="60032-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

