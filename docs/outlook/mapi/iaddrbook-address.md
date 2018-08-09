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
ms.openlocfilehash: 10f8f2cf44bf1a8e00f8c2b1a76826db5fc07161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766856"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="09c6b-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="09c6b-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="09c6b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09c6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09c6b-105">Exibe a caixa de diálogo do catálogo de endereços do Outlook.</span><span class="sxs-lookup"><span data-stu-id="09c6b-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="09c6b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09c6b-106">Parameters</span></span>

 <span data-ttu-id="09c6b-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="09c6b-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="09c6b-108">[além, out] Um ponteiro para um identificador da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="09c6b-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="09c6b-109">Na entrada, um identificador da janela sempre deve ser passado.</span><span class="sxs-lookup"><span data-stu-id="09c6b-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="09c6b-110">Na saída, se o membro **ulFlags** do parâmetro _lpAdrParms_ estiver definido como DIALOG_SDI, o identificador da janela da caixa de diálogo sem janela restrita é retornado.</span><span class="sxs-lookup"><span data-stu-id="09c6b-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="09c6b-111">Consulte os comentários.</span><span class="sxs-lookup"><span data-stu-id="09c6b-111">See Remarks.</span></span> 
    
 <span data-ttu-id="09c6b-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="09c6b-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="09c6b-113">[além, out] Um ponteiro para uma estrutura [ADRPARM](adrparm.md) que controla a apresentação e o comportamento da caixa de diálogo endereço.</span><span class="sxs-lookup"><span data-stu-id="09c6b-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="09c6b-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="09c6b-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="09c6b-115">[além, out] Um ponteiro para um ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém informações do destinatário.</span><span class="sxs-lookup"><span data-stu-id="09c6b-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="09c6b-116">Na entrada, esse parâmetro pode ser NULL ou apontar para um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="09c6b-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="09c6b-117">Na saída, este parâmetro aponta para um ponteiro para informações do destinatário válidos.</span><span class="sxs-lookup"><span data-stu-id="09c6b-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="09c6b-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="09c6b-118">Return value</span></span>

<span data-ttu-id="09c6b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="09c6b-119">S_OK</span></span> 
  
> <span data-ttu-id="09c6b-120">A caixa de diálogo endereço comuns com êxito foi exibida.</span><span class="sxs-lookup"><span data-stu-id="09c6b-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09c6b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="09c6b-121">Remarks</span></span>

<span data-ttu-id="09c6b-122">Se o membro **ulFlags** do parâmetro _lpAdrParms_ estiver definido como DIALOG_SDI prevendo o retorno da alça de janela da caixa de diálogo sem janela restrita na saída, ele é ignorado no Outlook; a versão modal da caixa de diálogo sempre é mostrada nos clientes não do Outlook.</span><span class="sxs-lookup"><span data-stu-id="09c6b-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="09c6b-123">A estrutura **ADRLIST** passada volta pelo MAPI para o chamador através do parâmetro _lppAdrList_ contém uma matriz de estruturas [ADRENTRY](adrentry.md) , uma estrutura de cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="09c6b-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="09c6b-124">Quando passados ao método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) de uma mensagem de saída no parâmetro _lpMods_ , a estrutura **ADRLIST** pode ser usada para atualizar sua lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="09c6b-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="09c6b-125">Cada estrutura **ADRENTRY** na estrutura **ADRLIST** contém zero ou mais estruturas de [SPropValue](spropvalue.md) , uma estrutura para cada propriedade definida para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="09c6b-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="09c6b-126">Pode haver zero estruturas **SPropValue** quando a caixa de diálogo apresentada pelo método **endereço** é usada para remover um destinatário.</span><span class="sxs-lookup"><span data-stu-id="09c6b-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="09c6b-127">Quando houver uma ou mais estruturas de **SPropValue** , a estrutura **ADRENTRY** correspondente é usada para adicionar ou atualizar um destinatário.</span><span class="sxs-lookup"><span data-stu-id="09c6b-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="09c6b-128">O destinatário pode ser resolvido, que indica que uma das estruturas **SPropValue** descreve a propriedade de **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) do destinatário, ou não resolvidos, que indica que a propriedade **PR_ENTRYID** é ausente.</span><span class="sxs-lookup"><span data-stu-id="09c6b-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="09c6b-129">Além das **PR_ENTRYID**, destinatários resolvidos incluem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="09c6b-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="09c6b-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="09c6b-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="09c6b-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="09c6b-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="09c6b-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="09c6b-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="09c6b-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="09c6b-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="09c6b-134">A estrutura **ADRLIST** que o chamador passa nas pode ser um tamanho diferente da estrutura de MAPI retorna.</span><span class="sxs-lookup"><span data-stu-id="09c6b-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="09c6b-135">Se o MAPI deve retornar uma estrutura maior de **ADRLIST** , ele libera a estrutura original e aloca um novo.</span><span class="sxs-lookup"><span data-stu-id="09c6b-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="09c6b-136">Quando você alocar memória para a estrutura **ADRLIST** , alocar a memória para cada estrutura **SPropValue** separadamente.</span><span class="sxs-lookup"><span data-stu-id="09c6b-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="09c6b-137">Para obter mais informações sobre como alocar e liberar **ADRLIST** estruturas, consulte [Gerenciando memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="09c6b-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="09c6b-138">**Endereço** retorna imediatamente se o sinalizador DIALOG_SDI é definido no membro **ulFlags** da estrutura **ADRPARM** no parâmetro _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="09c6b-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="09c6b-139">O sinalizador DIALOG_SDI é ignorado para clientes não do Outlook.</span><span class="sxs-lookup"><span data-stu-id="09c6b-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="09c6b-140">Se DIALOG_SDI será ignorada, a versão modal da caixa de diálogo será exibida e um ponteiro para uma alça não deve ser esperado em _lpulUIParam_.</span><span class="sxs-lookup"><span data-stu-id="09c6b-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="09c6b-141">**Endereço** suporta as sequências de caracteres Unicode na estrutura de **ADRPARM** se AB_UNICODEUI foi especificado no membro **ulFlags** **ADRPARM** no parâmetro _lpAdrParms_ e oferece suporte a cadeias de caracteres Unicode no ** ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="09c6b-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="09c6b-142">As cadeias de caracteres Unicode são convertidas para o formato de cadeia de caracteres (MBCS) caracteres multibyte antes que eles sejam exibidos na caixa de diálogo do catálogo de endereços do Outlook.</span><span class="sxs-lookup"><span data-stu-id="09c6b-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09c6b-143">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="09c6b-143">MFCMAPI reference</span></span>

<span data-ttu-id="09c6b-144">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="09c6b-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09c6b-145">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="09c6b-145">**File**</span></span>|<span data-ttu-id="09c6b-146">**Function**</span><span class="sxs-lookup"><span data-stu-id="09c6b-146">**Function**</span></span>|<span data-ttu-id="09c6b-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="09c6b-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09c6b-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="09c6b-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="09c6b-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="09c6b-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="09c6b-150">MFCMAPI usa o método de **endereço** para permitir que o usuário selecione qual caixa de correio para abrir.</span><span class="sxs-lookup"><span data-stu-id="09c6b-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09c6b-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="09c6b-151">See also</span></span>



[<span data-ttu-id="09c6b-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="09c6b-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="09c6b-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="09c6b-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="09c6b-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="09c6b-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="09c6b-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="09c6b-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="09c6b-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="09c6b-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="09c6b-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="09c6b-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="09c6b-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="09c6b-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="09c6b-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="09c6b-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="09c6b-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="09c6b-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="09c6b-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="09c6b-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="09c6b-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="09c6b-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="09c6b-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="09c6b-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="09c6b-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="09c6b-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="09c6b-165">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="09c6b-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="09c6b-166">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="09c6b-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

