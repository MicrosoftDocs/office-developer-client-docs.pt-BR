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
ms.openlocfilehash: 524bbfe5f40a66585fb4ed4463b057ca6a0c881a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586799"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="ac8e4-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="ac8e4-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="ac8e4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac8e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac8e4-105">Exibe a caixa de diálogo endereço comuns.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="ac8e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac8e4-106">Parameters</span></span>

 <span data-ttu-id="ac8e4-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ac8e4-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="ac8e4-108">[além, out] Um ponteiro para o identificador da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="ac8e4-109">Na entrada, um identificador da janela sempre deve ser passado.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="ac8e4-110">Na saída, se o sinalizador DIALOG_SDI é definido na estrutura [ADRPARM](adrparm.md) apontada pelo parâmetro _lpAdrParms_ , o identificador da janela da caixa de diálogo sem janela restrita é retornado.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="ac8e4-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="ac8e4-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="ac8e4-112">[além, out] Um ponteiro para uma estrutura **ADRPARM** que controla a apresentação e o comportamento da caixa de diálogo endereço.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="ac8e4-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="ac8e4-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="ac8e4-114">[além, out] Um ponteiro para um ponteiro para uma lista de endereços.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="ac8e4-115">Na entrada, esta lista é a lista atual de destinatários em uma mensagem ou NULL, se existir lista desse tipo.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="ac8e4-116">Na saída, _lppAdrList_ aponta para uma lista atualizada de destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ac8e4-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ac8e4-117">Return value</span></span>

<span data-ttu-id="ac8e4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac8e4-118">S_OK</span></span> 
  
> <span data-ttu-id="ac8e4-119">A caixa de diálogo de endereço com êxito foi exibida.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac8e4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac8e4-120">Remarks</span></span>

<span data-ttu-id="ac8e4-121">O método **IMAPISupport::Address** é implementado para objetos de suporte do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="ac8e4-122">Provedores de catálogo de endereço chamarem **endereço** para criar ou atualizar uma lista de destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="ac8e4-123">Cada destinatário é descrito em uma estrutura [ADRENTRY](adrentry.md) que está incluída na estrutura [ADRLIST](adrlist.md) apontada pelo parâmetro _lppAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="ac8e4-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="ac8e4-124">A estrutura **ADRENTRY** contém uma matriz de valores de propriedade de destinatário, um dos quais é o tipo do destinatário ou propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ac8e4-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="ac8e4-125">Essa estrutura **ADRLIST** pode ser passada para um cliente para usar como o parâmetro _lpMods_ em uma chamada para [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span><span class="sxs-lookup"><span data-stu-id="ac8e4-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="ac8e4-126">Cada destinatário na estrutura de **ADRLIST** pode ser seja resolvido, que indica que um dos seus valores de propriedade é sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou não resolvidos, que indica que a propriedade **PR_ENTRYID** é ausente.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="ac8e4-127">Além das **PR_ENTRYID**, destinatários resolvidos incluem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="ac8e4-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="ac8e4-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="ac8e4-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="ac8e4-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac8e4-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="ac8e4-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac8e4-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="ac8e4-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac8e4-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="ac8e4-132">Destinatários não resolvidos normalmente incluem somente **PR_DISPLAY_NAME** e **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac8e4-133">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ac8e4-133">Notes to callers</span></span>

<span data-ttu-id="ac8e4-134">A estrutura **ADRLIST** que o chamador passa nas pode ser um tamanho diferente da estrutura de MAPI retorna.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="ac8e4-135">Quando você alocar memória para a estrutura **ADRLIST** , alocar a memória para cada estrutura [SPropValue](spropvalue.md) separadamente.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="ac8e4-136">Use os ponteiros para as funções de alocação de memória MAPI passados para sua função [ABProviderInit](abproviderinit.md) para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="ac8e4-137">Alocar memória com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para **ADRLIST** e cada estrutura de valor de propriedade nas estruturas **ADRENTRY** em **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="ac8e4-138">Se o **endereço** deve retornar uma estrutura de **ADRLIST** maior, ou se você tiver passado NULL para _lppAdrList_, o **endereço** libera a estrutura original e aloca um novo.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="ac8e4-139">**Endereço** também aloca estruturas de valor de propriedade adicional na estrutura de **ADRLIST** e libera as antigas conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="ac8e4-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="ac8e4-140">Para obter mais informações sobre como a memória é gerenciada para estruturas **ADRLIST** , consulte [Gerenciando memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="ac8e4-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="ac8e4-141">**Endereço** retorna imediatamente se o sinalizador DIALOG_SDI foi definido na estrutura **ADRPARM** no parâmetro _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="ac8e4-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac8e4-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac8e4-142">See also</span></span>



[<span data-ttu-id="ac8e4-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="ac8e4-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="ac8e4-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="ac8e4-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="ac8e4-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ac8e4-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="ac8e4-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="ac8e4-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="ac8e4-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="ac8e4-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="ac8e4-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="ac8e4-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="ac8e4-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="ac8e4-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="ac8e4-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ac8e4-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ac8e4-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="ac8e4-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="ac8e4-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ac8e4-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ac8e4-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="ac8e4-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="ac8e4-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ac8e4-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ac8e4-155">Propriedade canônico de PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="ac8e4-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="ac8e4-156">Propriedade canônico de PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="ac8e4-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="ac8e4-157">Propriedade canônico de PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="ac8e4-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="ac8e4-158">Propriedade canônico PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="ac8e4-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="ac8e4-159">Propriedade canônico de PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="ac8e4-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="ac8e4-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ac8e4-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="ac8e4-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="ac8e4-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="ac8e4-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac8e4-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="ac8e4-163">Gerenciando memória para ADRLIST e estruturas de SRowSet</span><span class="sxs-lookup"><span data-stu-id="ac8e4-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

