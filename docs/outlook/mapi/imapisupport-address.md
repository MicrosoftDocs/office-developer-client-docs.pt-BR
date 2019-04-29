---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407316"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="18ada-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="18ada-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="18ada-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18ada-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18ada-105">Exibe a caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="18ada-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="18ada-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18ada-106">Parameters</span></span>

 <span data-ttu-id="18ada-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="18ada-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="18ada-108">[in, out] Um ponteiro para o identificador da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="18ada-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="18ada-109">Na entrada, um identificador de janela deve sempre ser aprovado.</span><span class="sxs-lookup"><span data-stu-id="18ada-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="18ada-110">Na saída, se o sinalizador DIALOG_SDI estiver definido na estrutura [ADRPARM](adrparm.md) apontada pelo parâmetro _lpAdrParms_ , o identificador de janela da caixa de diálogo sem-modo será retornado.</span><span class="sxs-lookup"><span data-stu-id="18ada-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="18ada-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="18ada-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="18ada-112">[in, out] Um ponteiro para uma estrutura **ADRPARM** que controla a apresentação e o comportamento da caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="18ada-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="18ada-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="18ada-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="18ada-114">[in, out] Um ponteiro para um ponteiro para uma lista de endereços.</span><span class="sxs-lookup"><span data-stu-id="18ada-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="18ada-115">Na entrada, essa lista é a lista atual de destinatários em uma mensagem ou nulo, se não houver essa lista.</span><span class="sxs-lookup"><span data-stu-id="18ada-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="18ada-116">Na saída, _lppAdrList_ aponta para uma lista atualizada de destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="18ada-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="18ada-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="18ada-117">Return value</span></span>

<span data-ttu-id="18ada-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="18ada-118">S_OK</span></span> 
  
> <span data-ttu-id="18ada-119">A caixa de diálogo endereço foi exibida com êxito.</span><span class="sxs-lookup"><span data-stu-id="18ada-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18ada-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="18ada-120">Remarks</span></span>

<span data-ttu-id="18ada-121">O método **IMAPISupport:: address** é implementado para objetos de suporte do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="18ada-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="18ada-122">Os provedores de catálogo de endereços chamam o **endereço** para criar ou atualizar uma lista de destinatários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="18ada-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="18ada-123">Cada destinatário é descrito em uma estrutura [ADRENTRY](adrentry.md) que é incluída na estrutura [das ADRLIST](adrlist.md) indicada pelo parâmetro _lppAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="18ada-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="18ada-124">A estrutura **ADRENTRY** contém uma matriz de valores de propriedade de destinatário, uma das quais é o tipo do destinatário ou a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="18ada-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="18ada-125">Essa estrutura **das ADRLIST** pode ser passada para um cliente para uso como o parâmetro _lpMods_ em uma chamada para [IMessage:: ModifyRecipients](imessage-modifyrecipients.md).</span><span class="sxs-lookup"><span data-stu-id="18ada-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="18ada-126">Cada destinatário na estrutura **das ADRLIST** pode ser resolvido, o que indica que um de seus valores de propriedade é sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou não resolvido, o que indica que a propriedade **PR_ENTRYID** é encontrado.</span><span class="sxs-lookup"><span data-stu-id="18ada-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="18ada-127">Além de **PR_ENTRYID**, os destinatários resolvidos incluem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="18ada-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="18ada-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="18ada-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="18ada-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="18ada-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="18ada-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="18ada-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="18ada-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="18ada-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="18ada-132">Os destinatários não resolvidos normalmente incluem apenas **PR_DISPLAY_NAME** e **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="18ada-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="18ada-133">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="18ada-133">Notes to callers</span></span>

<span data-ttu-id="18ada-134">A estrutura **das ADRLIST** que o chamador transmite pode ser um tamanho diferente da estrutura que o MAPI retorna.</span><span class="sxs-lookup"><span data-stu-id="18ada-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="18ada-135">Ao alocar memória para a estrutura **das ADRLIST** , aloque a memória de cada estrutura do [SPropValue](spropvalue.md) separadamente.</span><span class="sxs-lookup"><span data-stu-id="18ada-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="18ada-136">Use os ponteiros para as funções de alocação de memória MAPI passadas para sua função [ABProviderInit](abproviderinit.md) para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="18ada-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="18ada-137">Alocar memória com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para **das ADRLIST** e cada estrutura de valor de propriedade nas estruturas **ADRENTRY** no **das ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="18ada-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="18ada-138">Se o **endereço** deve retornar uma estrutura **das ADRLIST** maior, ou se você tiver passado nulo para o _lppAdrList_, o **endereço** liberará a estrutura original e alocará uma nova.</span><span class="sxs-lookup"><span data-stu-id="18ada-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="18ada-139">O **endereço** também aloca estruturas de valor de propriedade adicionais na estrutura **das ADRLIST** e libera as antigas conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="18ada-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="18ada-140">Para obter mais informações sobre como a memória é gerenciada para estruturas **das ADRLIST** , consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="18ada-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="18ada-141">O **endereço** retorna imediatamente se o sinalizador DIALOG_SDI foi definido na estrutura **ADRPARM** no parâmetro _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="18ada-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="18ada-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="18ada-142">See also</span></span>



[<span data-ttu-id="18ada-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="18ada-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="18ada-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="18ada-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="18ada-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="18ada-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="18ada-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="18ada-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="18ada-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="18ada-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="18ada-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="18ada-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="18ada-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="18ada-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="18ada-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="18ada-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="18ada-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="18ada-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="18ada-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="18ada-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="18ada-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="18ada-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="18ada-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="18ada-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="18ada-155">Propriedade canônica PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="18ada-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="18ada-156">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="18ada-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="18ada-157">Propriedade canônica PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="18ada-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="18ada-158">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="18ada-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="18ada-159">Propriedade canônica PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="18ada-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="18ada-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="18ada-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="18ada-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="18ada-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="18ada-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="18ada-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="18ada-163">Gerenciando memória para estruturas das ADRLIST e SRowSet</span><span class="sxs-lookup"><span data-stu-id="18ada-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

