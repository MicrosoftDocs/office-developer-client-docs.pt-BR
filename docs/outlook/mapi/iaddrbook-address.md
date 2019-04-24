---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348843"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="303d6-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="303d6-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="303d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="303d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="303d6-105">Exibe a caixa de diálogo catálogo de endereços do Outlook.</span><span class="sxs-lookup"><span data-stu-id="303d6-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="303d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="303d6-106">Parameters</span></span>

 <span data-ttu-id="303d6-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="303d6-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="303d6-108">[in, out] Um ponteiro para um identificador da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="303d6-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="303d6-109">Na entrada, um identificador de janela deve sempre ser aprovado.</span><span class="sxs-lookup"><span data-stu-id="303d6-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="303d6-110">Na saída, se o membro **parâmetroulflags** do parâmetro _lpAdrParms_ for definido como DIALOG_SDI, o identificador de janela da caixa de diálogo sem-modo será retornado.</span><span class="sxs-lookup"><span data-stu-id="303d6-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="303d6-111">Consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="303d6-111">See Remarks.</span></span> 
    
 <span data-ttu-id="303d6-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="303d6-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="303d6-113">[in, out] Um ponteiro para uma estrutura [ADRPARM](adrparm.md) que controla a apresentação e o comportamento da caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="303d6-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="303d6-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="303d6-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="303d6-115">[in, out] Um ponteiro para um ponteiro para uma estrutura [das ADRLIST](adrlist.md) que contém informações do destinatário.</span><span class="sxs-lookup"><span data-stu-id="303d6-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="303d6-116">Na entrada, esse parâmetro pode ser nulo ou apontar para um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="303d6-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="303d6-117">Na saída, esse parâmetro aponta para um ponteiro para obter informações válidas do destinatário.</span><span class="sxs-lookup"><span data-stu-id="303d6-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="303d6-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="303d6-118">Return value</span></span>

<span data-ttu-id="303d6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="303d6-119">S_OK</span></span> 
  
> <span data-ttu-id="303d6-120">A caixa de diálogo endereço comum foi exibida com êxito.</span><span class="sxs-lookup"><span data-stu-id="303d6-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="303d6-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="303d6-121">Remarks</span></span>

<span data-ttu-id="303d6-122">Se o membro **parâmetroulflags** do parâmetro _lpAdrParms_ estiver definido como DIALOG_SDI antecipando o retorno do identificador de janela da caixa de diálogo sem-modo na saída, ele será ignorado no Outlook; a versão modal da caixa de diálogo sempre é mostrada em clientes não-Outlook.</span><span class="sxs-lookup"><span data-stu-id="303d6-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="303d6-123">A estrutura **das ADRLIST** passada de volta por MAPI para o chamador através do parâmetro _lppAdrList_ contém uma matriz de estruturas do [ADRENTRY](adrentry.md) , uma estrutura para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="303d6-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="303d6-124">Quando passadas para o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) de uma mensagem de saída no parâmetro _lpMods_ , a estrutura **das ADRLIST** pode ser usada para atualizar sua lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="303d6-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="303d6-125">Cada estrutura **ADRENTRY** na estrutura **das ADRLIST** contém zero ou mais estruturas de [SPropValue](spropvalue.md) , uma estrutura para cada conjunto de propriedades para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="303d6-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="303d6-126">Pode haver nenhuma estrutura **SPropValue** quando a caixa de diálogo apresentada pelo método **Address** é usada para remover um destinatário.</span><span class="sxs-lookup"><span data-stu-id="303d6-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="303d6-127">Quando há uma ou mais estruturas **SPropValue** , a estrutura **ADRENTRY** correspondente é usada para adicionar ou atualizar um destinatário.</span><span class="sxs-lookup"><span data-stu-id="303d6-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="303d6-128">O destinatário pode ser resolvido, o que indica que uma das estruturas **SPropValue** descreve a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) do destinatário, ou não resolvida, que indica que a propriedade **PR_ENTRYID** é encontrado.</span><span class="sxs-lookup"><span data-stu-id="303d6-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="303d6-129">Além de **PR_ENTRYID**, os destinatários resolvidos incluem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="303d6-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="303d6-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="303d6-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="303d6-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="303d6-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="303d6-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="303d6-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="303d6-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="303d6-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="303d6-134">A estrutura **das ADRLIST** que o chamador transmite pode ser um tamanho diferente da estrutura que o MAPI retorna.</span><span class="sxs-lookup"><span data-stu-id="303d6-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="303d6-135">Se o MAPI deve retornar uma estrutura **das ADRLIST** maior, ele libera a estrutura original e aloca um novo.</span><span class="sxs-lookup"><span data-stu-id="303d6-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="303d6-136">Ao alocar memória para a estrutura **das ADRLIST** , aloque a memória de cada estrutura do **SPropValue** separadamente.</span><span class="sxs-lookup"><span data-stu-id="303d6-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="303d6-137">Para obter mais informações sobre como alocar e liberar estruturas do **das ADRLIST** , consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="303d6-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="303d6-138">O **endereço** retorna imediatamente se o sinalizador DIALOG_SDI estiver definido no membro **Parâmetroulflags** da estrutura **ADRPARM** no parâmetro _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="303d6-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="303d6-139">O sinalizador DIALOG_SDI é ignorado para clientes que não são do Outlook.</span><span class="sxs-lookup"><span data-stu-id="303d6-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="303d6-140">Se DIALOG_SDI for ignorado, a versão modal da caixa de diálogo será exibida e um ponteiro para um identificador não deverá ser esperado no _lpulUIParam_.</span><span class="sxs-lookup"><span data-stu-id="303d6-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="303d6-141">O **endereço** oferece suporte a cadeias de caracteres Unicode na estrutura **ADRPARM** se AB_UNICODEUI foi especificado no membro **Parâmetroulflags** de **ADRPARM** no parâmetro _LpAdrParms_ e oferece suporte a cadeias de caracteres Unicode no \*\* DAS ADRLIST\*\*.</span><span class="sxs-lookup"><span data-stu-id="303d6-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="303d6-142">As cadeias de caracteres Unicode são convertidas no formato MBCS (cadeia de caracteres multibyte) antes de serem exibidas na caixa de diálogo catálogo de endereços do Outlook.</span><span class="sxs-lookup"><span data-stu-id="303d6-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="303d6-143">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="303d6-143">MFCMAPI reference</span></span>

<span data-ttu-id="303d6-144">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="303d6-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="303d6-145">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="303d6-145">**File**</span></span>|<span data-ttu-id="303d6-146">**Função**</span><span class="sxs-lookup"><span data-stu-id="303d6-146">**Function**</span></span>|<span data-ttu-id="303d6-147">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="303d6-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="303d6-148">MAPIStoreFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="303d6-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="303d6-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="303d6-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="303d6-150">MFCMAPI usa o método **Address** para permitir que o usuário selecione qual caixa de correio abrir.</span><span class="sxs-lookup"><span data-stu-id="303d6-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="303d6-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="303d6-151">See also</span></span>



[<span data-ttu-id="303d6-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="303d6-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="303d6-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="303d6-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="303d6-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="303d6-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="303d6-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="303d6-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="303d6-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="303d6-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="303d6-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="303d6-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="303d6-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="303d6-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="303d6-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="303d6-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="303d6-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="303d6-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="303d6-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="303d6-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="303d6-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="303d6-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="303d6-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="303d6-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="303d6-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="303d6-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="303d6-165">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="303d6-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="303d6-166">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="303d6-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

