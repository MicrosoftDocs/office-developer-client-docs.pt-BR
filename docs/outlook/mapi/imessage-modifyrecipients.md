---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0735008575db5e1cab62dbde4b699b15e04cedb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567283"
---
# <a name="imessagemodifyrecipients"></a><span data-ttu-id="f666f-103">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="f666f-103">IMessage::ModifyRecipients</span></span>

  
  
<span data-ttu-id="f666f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f666f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f666f-105">Adiciona, exclui ou modifica os destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f666f-105">Adds, deletes, or modifies message recipients.</span></span>
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a><span data-ttu-id="f666f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f666f-106">Parameters</span></span>

 <span data-ttu-id="f666f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f666f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f666f-108">[in] Bitmask dos sinalizadores que controla as alterações do destinatários.</span><span class="sxs-lookup"><span data-stu-id="f666f-108">[in] Bitmask of flags that controls the recipient changes.</span></span> <span data-ttu-id="f666f-109">Se o zero é passado para o parâmetro _ulFlags_ , **ModifyRecipients** substitui todos os destinatários existentes com a lista de destinatários apontada pelo parâmetro _lpMods_ .</span><span class="sxs-lookup"><span data-stu-id="f666f-109">If zero is passed for the  _ulFlags_ parameter, **ModifyRecipients** replaces all existing recipients with the recipient list pointed to by the  _lpMods_ parameter.</span></span> <span data-ttu-id="f666f-110">Sinalizadores a seguir podem ser definidos para _ulFlags_:</span><span class="sxs-lookup"><span data-stu-id="f666f-110">The following flags can be set for  _ulFlags_:</span></span>
    
<span data-ttu-id="f666f-111">MODRECIP_ADD</span><span class="sxs-lookup"><span data-stu-id="f666f-111">MODRECIP_ADD</span></span> 
  
> <span data-ttu-id="f666f-112">Os destinatários apontados pelo parâmetro _lpMods_ devem ser adicionados à lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="f666f-112">The recipients pointed to by the  _lpMods_ parameter should be added to the recipient list.</span></span> 
    
<span data-ttu-id="f666f-113">MODRECIP_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f666f-113">MODRECIP_MODIFY</span></span> 
  
> <span data-ttu-id="f666f-114">Os destinatários apontados pelo parâmetro _lpMods_ devem substituir destinatários existentes.</span><span class="sxs-lookup"><span data-stu-id="f666f-114">The recipients pointed to by the  _lpMods_ parameter should replace existing recipients.</span></span> <span data-ttu-id="f666f-115">Todas as propriedades existentes são substituídas por aqueles na estrutura de [ADRENTRY](adrentry.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="f666f-115">All of the existing properties are replaced by those in the corresponding [ADRENTRY](adrentry.md) structure.</span></span> 
    
<span data-ttu-id="f666f-116">MODRECIP_REMOVE</span><span class="sxs-lookup"><span data-stu-id="f666f-116">MODRECIP_REMOVE</span></span> 
  
> <span data-ttu-id="f666f-117">Destinatários existentes devem ser removidos da lista de destinatários usando, como um índice, a propriedade **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) incluída na matriz de valor de propriedade de cada entrada do destinatário no parâmetro _lpMods_ .</span><span class="sxs-lookup"><span data-stu-id="f666f-117">Existing recipients should be removed from the recipient list using as an index the **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) property included in the property value array of each recipient entry in the  _lpMods_ parameter.</span></span> 
    
 <span data-ttu-id="f666f-118">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="f666f-118">_lpMods_</span></span>
  
> <span data-ttu-id="f666f-119">[in] Ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém uma lista de destinatários para ser adicionado, excluído ou modificado na mensagem.</span><span class="sxs-lookup"><span data-stu-id="f666f-119">[in] Pointer to an [ADRLIST](adrlist.md) structure that contains a list of recipients to be added, deleted, or modified in the message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f666f-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f666f-120">Return value</span></span>

<span data-ttu-id="f666f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="f666f-121">S_OK</span></span> 
  
> <span data-ttu-id="f666f-122">A lista de destinatários com êxito foi modificada.</span><span class="sxs-lookup"><span data-stu-id="f666f-122">The recipient list was successfully modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f666f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f666f-123">Remarks</span></span>

<span data-ttu-id="f666f-124">O método **IMessage::ModifyRecipients** altera a lista de destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f666f-124">The **IMessage::ModifyRecipients** method changes the message's recipient list.</span></span> <span data-ttu-id="f666f-125">É a partir dessa lista, mantida em uma estrutura [ADRLIST](adrlist.md) , que a tabela de destinatário é criada.</span><span class="sxs-lookup"><span data-stu-id="f666f-125">It is from this list, held in an [ADRLIST](adrlist.md) structure, that the recipient table is built.</span></span> 
  
<span data-ttu-id="f666f-126">A estrutura **ADRLIST** contém uma estrutura [ADRENTRY](adrentry.md) para cada destinatário e cada estrutura **ADRENTRY** contém uma matriz de valores de propriedades descrevendo as propriedades do destinatário.</span><span class="sxs-lookup"><span data-stu-id="f666f-126">The **ADRLIST** structure contains one [ADRENTRY](adrentry.md) structure for each recipient and each **ADRENTRY** structure contains an array of property values describing the recipient properties.</span></span> 
  
<span data-ttu-id="f666f-127">Destinatários na estrutura de **ADRLIST** podem ser resolvidos ou não resolvidos.</span><span class="sxs-lookup"><span data-stu-id="f666f-127">Recipients in the **ADRLIST** structure can be resolved or unresolved.</span></span> <span data-ttu-id="f666f-128">A diferença é o número e o tipo de propriedades que são incluídos.</span><span class="sxs-lookup"><span data-stu-id="f666f-128">The difference is in the number and type of properties that are included.</span></span> <span data-ttu-id="f666f-129">Um destinatário não resolvido contém somente as propriedades de **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) e **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) enquanto um destinatário resolvido contém essas duas propriedades plus **PR_ADDRTYPE **([PidTagAddressType](pidtagaddresstype-canonical-property.md)) e **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f666f-129">An unresolved recipient contains only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) properties while a resolved recipient contains those two properties plus **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span> <span data-ttu-id="f666f-130">Se **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) estiver disponível, ele pode ser incluído também.</span><span class="sxs-lookup"><span data-stu-id="f666f-130">If **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is available, it can be included also.</span></span>
  
<span data-ttu-id="f666f-131">No momento em que uma mensagem é enviada, ele deve incluir somente os destinatários resolvidos na sua lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="f666f-131">By the time a message is submitted, it must include only resolved recipients in its recipient list.</span></span> <span data-ttu-id="f666f-132">Destinatários não resolvidos causam NDRs seja criado e enviado ao remetente original da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f666f-132">Unresolved recipients cause nondelivery reports to be created and sent to the original sender of the message.</span></span> <span data-ttu-id="f666f-133">Para obter mais informações sobre o processo de resolução de nomes da perspectiva do cliente, consulte a [resolução de nomes](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="f666f-133">For more information about the name resolution process from the client perspective, see [Resolving a Name](resolving-a-recipient-name.md).</span></span> <span data-ttu-id="f666f-134">Para obter mais informações da perspectiva do provedor de catálogo de endereços, consulte [Implementando a resolução de nome](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="f666f-134">For more information from the perspective of the address book provider, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="f666f-135">Além dos destinatários resolvidos e não resolvidos, um destinatário pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="f666f-135">In addition to resolved and unresolved recipients, a recipient can be NULL.</span></span> <span data-ttu-id="f666f-136">O membro **cValues** da estrutura **ADRENTRY** para o destinatário está definido como zero e o membro **rgPropVals** é definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="f666f-136">The **cValues** member of the **ADRENTRY** structure for the recipient is set to zero and the **rgPropVals** member is set to NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f666f-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f666f-137">Notes to callers</span></span>

<span data-ttu-id="f666f-138">Você pode criar uma lista de destinatários chamando [IAddrBook::Address](imapisupport-address.md) para exibir a caixa de diálogo comuns e solicita ao usuário para selecionar entradas.</span><span class="sxs-lookup"><span data-stu-id="f666f-138">You can create a recipient list by calling [IAddrBook::Address](imapisupport-address.md) to display the common dialog box and prompt the user to select entries.</span></span> <span data-ttu-id="f666f-139">A lista de endereços apontada pelo parâmetro _lppAdrList_ como **endereço** pode ser passada para **ModifyRecipients** como o parâmetro _lpMods_ .</span><span class="sxs-lookup"><span data-stu-id="f666f-139">The address list pointed to by the  _lppAdrList_ parameter to **Address** can be passed to **ModifyRecipients** as the  _lpMods_ parameter.</span></span> 
  
<span data-ttu-id="f666f-140">Quando você especificar propriedades para um destinatário na estrutura [ADRLIST](adrlist.md) , inclua todas as propriedades do destinatário, não apenas aqueles novos ou alterados.</span><span class="sxs-lookup"><span data-stu-id="f666f-140">When you specify properties for a recipient in the [ADRLIST](adrlist.md) structure, include all of the recipient's properties, not only the new or changed ones.</span></span> <span data-ttu-id="f666f-141">Quando um destinatário é modificado, todas as propriedades não incluídas na estrutura **ADRLIST** são excluídas.</span><span class="sxs-lookup"><span data-stu-id="f666f-141">When a recipient is modified, any properties not included in the **ADRLIST** structure are deleted.</span></span> <span data-ttu-id="f666f-142">Para recuperar o conjunto atual de propriedades para todos os destinatários da mensagem, chame [GetRecipientTable](imessage-getrecipienttable.md) e recuperar todas as linhas.</span><span class="sxs-lookup"><span data-stu-id="f666f-142">To retrieve the current set of properties for all of a message's recipients, call [GetRecipientTable](imessage-getrecipienttable.md) and retrieve all of the rows.</span></span> <span data-ttu-id="f666f-143">Como um **SRowSet** é idêntica em estrutura um **ADRLIST**, você pode usá-los de forma intercambiável.</span><span class="sxs-lookup"><span data-stu-id="f666f-143">Because an **SRowSet** is identical in structure to an **ADRLIST**, you can use them interchangeably.</span></span>
  
 <span data-ttu-id="f666f-144">**ModifyRecipients** substitui todas as entradas na lista de destinatários atual com as informações apontadas pela _lpMods_ quando nenhum dos sinalizadores estão definidos no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f666f-144">**ModifyRecipients** replaces all of the entries in the current recipient list with the information pointed to by  _lpMods_ when none of the flags are set in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f666f-145">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f666f-145">Notes to callers</span></span>

<span data-ttu-id="f666f-146">Quando você definir o sinalizador MODRECIP_MODIFY, **ModifyRecipients** substitui cada linha inteira de destinatário com a linha associada na estrutura [ADRLIST](adrlist.md) passada em _lpMods_.</span><span class="sxs-lookup"><span data-stu-id="f666f-146">When you set the MODRECIP_MODIFY flag, **ModifyRecipients** replaces each entire recipient row with the associated row in the [ADRLIST](adrlist.md) structure passed in  _lpMods_.</span></span> <span data-ttu-id="f666f-147">Tenha cuidado para especificar que todas as propriedades que um destinatário deve ter independentemente se eles foram alterados para impedir que está sendo excluído acidentalmente.</span><span class="sxs-lookup"><span data-stu-id="f666f-147">Be careful to specify all of the properties that a recipient should have regardless of whether they have changed to prevent them from being unintentionally deleted.</span></span>
  
<span data-ttu-id="f666f-148">Estas são algumas regras para definir as propriedades dos destinatários na estrutura de **ADRLIST** :</span><span class="sxs-lookup"><span data-stu-id="f666f-148">Following are some rules for setting the properties of the recipients in the **ADRLIST** structure:</span></span> 
  
- <span data-ttu-id="f666f-149">Não use PT_NULL como um tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f666f-149">Do not use PT_NULL as a property type.</span></span> <span data-ttu-id="f666f-150">**ModifyRecipients** retornará um erro quando se deparar com esse valor.</span><span class="sxs-lookup"><span data-stu-id="f666f-150">**ModifyRecipients** returns an error when encountering this value.</span></span> 
    
- <span data-ttu-id="f666f-151">Não use PT_ERROR como um tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f666f-151">Do not use PT_ERROR as a property type.</span></span> <span data-ttu-id="f666f-152">**ModifyRecipients** ignora esse valor.</span><span class="sxs-lookup"><span data-stu-id="f666f-152">**ModifyRecipients** ignores this value.</span></span> 
    
- <span data-ttu-id="f666f-153">Inclua a propriedade **PR_ROWID** para todos os destinatários quando você definir o sinalizador o MODRECIP_REMOVE ou MODRECIP_MODIFY no _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="f666f-153">Include the **PR_ROWID** property for all recipients when you set either the MODRECIP_REMOVE or MODRECIP_MODIFY flag in  _ulFlags_.</span></span> 
    
- <span data-ttu-id="f666f-154">Não inclua a propriedade **PR_ROWID** para qualquer um dos destinatários quando você definir o sinalizador MODRECIP_ADD no _ulFlags_ ou quando você passá zero em _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="f666f-154">Do not include the **PR_ROWID** property for any of the recipients when you set the MODRECIP_ADD flag in  _ulFlags_ or when you pass zero in  _ulFlags_.</span></span>
    
<span data-ttu-id="f666f-155">Se você incluir a propriedade **PR_ADDRTYPE** ou a propriedade **PR_EMAIL_ADDRESS** para um destinatário e uma ou ambas dessas propriedades são inconsistentes com o tipo de endereço e o endereço do destinatário, conforme identificado pelo **PR_ENTRYID**, o os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="f666f-155">If you include either the **PR_ADDRTYPE** property or **PR_EMAIL_ADDRESS** property for a recipient and one or both of these properties are inconsistent with the address type and address of the recipient as identified by **PR_ENTRYID**, the results are undefined.</span></span> <span data-ttu-id="f666f-156">Ou seja, há três possibilidades, dependendo do provedor de serviço:</span><span class="sxs-lookup"><span data-stu-id="f666f-156">That is, there are three possibilities, depending on the service provider:</span></span>
  
- <span data-ttu-id="f666f-157">A mensagem será entregue para o endereço descrito pelas propriedades **PR_ADDRTYPE** e **PR_EMAIL_ADDRESS** .</span><span class="sxs-lookup"><span data-stu-id="f666f-157">The message will be delivered to the address described by the **PR_ADDRTYPE** and **PR_EMAIL_ADDRESS** properties.</span></span> 
    
- <span data-ttu-id="f666f-158">A mensagem será entregue ao destinatário identificado pela **PR_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="f666f-158">The message will be delivered to the recipient identified by **PR_ENTRYID**.</span></span>
    
- <span data-ttu-id="f666f-159">A mensagem será declarada não entregue devido a ambiguidade das informações de endereço.</span><span class="sxs-lookup"><span data-stu-id="f666f-159">The message will be declared undeliverable due to the ambiguity of the address information.</span></span>
    
<span data-ttu-id="f666f-160">Use as regras de alocação descritas no [Gerenciamento de memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md) alocar memória para a lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="f666f-160">Use the allocation rules outlined in [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md) to allocate memory for the recipient list.</span></span> <span data-ttu-id="f666f-161">**ModifyRecipients** não liberar a estrutura **ADRLIST** nem qualquer uma das suas subestruturas.</span><span class="sxs-lookup"><span data-stu-id="f666f-161">**ModifyRecipients** does not free the **ADRLIST** structure nor any of its substructures.</span></span> <span data-ttu-id="f666f-162">A estrutura **ADRLIST** e cada estrutura [SPropValue](spropvalue.md) devem ser alocados separadamente usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , de forma que cada uma pode ser liberada individualmente.</span><span class="sxs-lookup"><span data-stu-id="f666f-162">The **ADRLIST** structure and each [SPropValue](spropvalue.md) structure must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function such that each can be freed individually.</span></span> <span data-ttu-id="f666f-163">Se o método requer espaço adicional para qualquer estrutura **SPropValue** , ele pode substituir a estrutura de **SPropValue** por um novo que posteriormente pode ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f666f-163">If the method requires additional space for any **SPropValue** structure, it can replace the **SPropValue** structure with a new one that can later be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span> <span data-ttu-id="f666f-164">A estrutura original de **SPropValue** também deve ser liberada usando **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="f666f-164">The original **SPropValue** structure should also be freed using **MAPIFreeBuffer**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f666f-165">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f666f-165">MFCMAPI reference</span></span>

<span data-ttu-id="f666f-166">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f666f-166">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f666f-167">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f666f-167">**File**</span></span>|<span data-ttu-id="f666f-168">**Function**</span><span class="sxs-lookup"><span data-stu-id="f666f-168">**Function**</span></span>|<span data-ttu-id="f666f-169">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f666f-169">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f666f-170">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f666f-170">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f666f-171">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="f666f-171">AddRecipient</span></span>  <br/> |<span data-ttu-id="f666f-172">MFCMAPI usa o método **IMessage::ModifyRecipients** para adicionar um novo destinatário a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f666f-172">MFCMAPI uses the **IMessage::ModifyRecipients** method to add a new recipient to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f666f-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="f666f-173">See also</span></span>



[<span data-ttu-id="f666f-174">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="f666f-174">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="f666f-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="f666f-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="f666f-176">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="f666f-176">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="f666f-177">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="f666f-177">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="f666f-178">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="f666f-178">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="f666f-179">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f666f-179">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f666f-180">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f666f-180">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="f666f-181">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f666f-181">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="f666f-182">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f666f-182">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

