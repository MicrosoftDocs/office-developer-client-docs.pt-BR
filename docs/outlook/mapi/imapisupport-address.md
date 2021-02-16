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
# <a name="imapisupportaddress"></a><span data-ttu-id="99953-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="99953-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="99953-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99953-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99953-105">Exibe a caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="99953-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="99953-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99953-106">Parameters</span></span>

 <span data-ttu-id="99953-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="99953-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="99953-108">[in, out] Um ponteiro para o alça da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="99953-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="99953-109">Na entrada, uma alça de janela sempre deve ser passada.</span><span class="sxs-lookup"><span data-stu-id="99953-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="99953-110">Na saída, se o sinalizador DIALOG_SDI for definido na estrutura [ADRPARM](adrparm.md) apontada pelo parâmetro  _lpAdrParms,_ a alça da janela da caixa de diálogo sem janela será retornada.</span><span class="sxs-lookup"><span data-stu-id="99953-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="99953-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="99953-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="99953-112">[in, out] Um ponteiro para uma **estrutura ADRPARM** que controla a apresentação e o comportamento da caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="99953-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="99953-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="99953-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="99953-114">[in, out] Um ponteiro para um ponteiro para uma lista de endereços.</span><span class="sxs-lookup"><span data-stu-id="99953-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="99953-115">Na entrada, essa lista é a lista atual de destinatários em uma mensagem ou NULL, caso essa lista não exista.</span><span class="sxs-lookup"><span data-stu-id="99953-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="99953-116">Na saída,  _lppAdrList_ aponta para uma lista atualizada de destinatários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="99953-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="99953-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="99953-117">Return value</span></span>

<span data-ttu-id="99953-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="99953-118">S_OK</span></span> 
  
> <span data-ttu-id="99953-119">A caixa de diálogo de endereço foi exibida com êxito.</span><span class="sxs-lookup"><span data-stu-id="99953-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99953-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="99953-120">Remarks</span></span>

<span data-ttu-id="99953-121">O **método IMAPISupport::Address** é implementado para objetos de suporte do provedor de agendas de endereços.</span><span class="sxs-lookup"><span data-stu-id="99953-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="99953-122">Os provedores de agendamento de endereços chamam **Address** para criar ou atualizar uma lista de destinatários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="99953-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="99953-123">Cada destinatário é descrito em uma estrutura [ADRENTRY](adrentry.md) incluída na estrutura [ADRLIST](adrlist.md) apontada pelo parâmetro _lppAdrList._</span><span class="sxs-lookup"><span data-stu-id="99953-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="99953-124">A **estrutura ADRENTRY** contém uma matriz de valores de propriedade de destinatário, um dos quais é o tipo do destinatário ou PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="99953-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="99953-125">Essa **estrutura ADRLIST** pode ser passada para um cliente para usar como o parâmetro  _lpMods_ em uma chamada para [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span><span class="sxs-lookup"><span data-stu-id="99953-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="99953-126">Cada destinatário na estrutura **ADRLIST** pode ser resolvido, o que indica que um de seus valores de propriedade é sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), ou não resolvido, o que indica que a propriedade **PR_ENTRYID** está ausente.</span><span class="sxs-lookup"><span data-stu-id="99953-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="99953-127">Além de **PR_ENTRYID** destinatários resolvidos, incluem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="99953-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="99953-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="99953-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="99953-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99953-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="99953-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99953-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="99953-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="99953-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="99953-132">Destinatários não resolvidos geralmente incluem apenas **PR_DISPLAY_NAME** e **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="99953-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="99953-133">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="99953-133">Notes to callers</span></span>

<span data-ttu-id="99953-134">A **estrutura ADRLIST** que o chamador passa pode ter um tamanho diferente da estrutura que o MAPI retorna.</span><span class="sxs-lookup"><span data-stu-id="99953-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="99953-135">Quando você alocar memória para **a estrutura ADRLIST,** aloce a memória para cada [estrutura SPropValue](spropvalue.md) separadamente.</span><span class="sxs-lookup"><span data-stu-id="99953-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="99953-136">Use os ponteiros para as funções de alocação de memória MAPI passadas para sua função [ABProviderInit](abproviderinit.md) para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="99953-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="99953-137">Aloque memória com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para **ADRLIST** e cada estrutura de valor de propriedade nas estruturas **ADRENTRY** em **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="99953-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="99953-138">Se **Address** deve retornar uma estrutura **ADRLIST** maior, ou se você tiver passado NULL para  _lppAdrList_, **Address** libera a estrutura original e aloca uma nova.</span><span class="sxs-lookup"><span data-stu-id="99953-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="99953-139">**O** endereço também aloca estruturas de valor de propriedade adicionais na estrutura **ADRLIST** e libera as antigas conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="99953-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="99953-140">Para obter mais informações sobre como a memória é gerenciada para estruturas **ADRLIST,** consulte Gerenciando memória [para estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="99953-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="99953-141">**Address** retorna imediatamente se o DIALOG_SDI sinalizador foi definido na estrutura **ADRPARM** no _parâmetro lpAdrParms._</span><span class="sxs-lookup"><span data-stu-id="99953-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99953-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="99953-142">See also</span></span>



[<span data-ttu-id="99953-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="99953-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="99953-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="99953-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="99953-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="99953-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="99953-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="99953-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="99953-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="99953-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="99953-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="99953-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="99953-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="99953-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="99953-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="99953-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="99953-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="99953-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="99953-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="99953-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="99953-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="99953-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="99953-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="99953-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="99953-155">Propriedade canônica PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="99953-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="99953-156">Propriedade canônica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="99953-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="99953-157">Propriedade canônica PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="99953-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="99953-158">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="99953-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="99953-159">Propriedade canônica PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="99953-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="99953-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="99953-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="99953-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="99953-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="99953-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="99953-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="99953-163">Gerenciando memória para estruturas ADRLIST e SRowSet</span><span class="sxs-lookup"><span data-stu-id="99953-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

