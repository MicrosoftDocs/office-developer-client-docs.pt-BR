---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405811"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="0c184-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="0c184-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="0c184-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c184-105">Executa a resolução de nome para uma ou mais entradas de destinatário.</span><span class="sxs-lookup"><span data-stu-id="0c184-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="0c184-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c184-106">Parameters</span></span>

 <span data-ttu-id="0c184-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="0c184-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="0c184-108">[in] Um ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que descrevem as propriedades a serem incluídas na estrutura [ADRLIST](adrlist.md) retornada pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="0c184-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="0c184-109">Para solicitar o conjunto padrão de propriedades do provedor, passe NULL no _parâmetro lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="0c184-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="0c184-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c184-110">_ulFlags_</span></span>
  
> <span data-ttu-id="0c184-111">[in] Uma bitmask de sinalizadores que controla o tipo de texto nas cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="0c184-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="0c184-112">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="0c184-112">The following flags can be set:</span></span>
    
<span data-ttu-id="0c184-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="0c184-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="0c184-114">Somente as combinações exatas de endereço proxy serão encontradas; parciais são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="0c184-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="0c184-115">Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="0c184-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="0c184-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="0c184-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="0c184-117">Somente o livro de endereços offline será usado para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="0c184-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="0c184-118">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="0c184-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="0c184-119">Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="0c184-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="0c184-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0c184-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0c184-121">As propriedades de cadeia de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0c184-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="0c184-122">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0c184-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="0c184-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="0c184-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="0c184-124">[in, out] Na entrada, um ponteiro para uma **estrutura ADRLIST** que contém a lista de destinatários a serem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="0c184-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="0c184-125">Na saída, um ponteiro para uma estrutura **ADRLIST** que contém os nomes resolvidos.</span><span class="sxs-lookup"><span data-stu-id="0c184-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="0c184-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="0c184-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="0c184-127">[in, out] Um ponteiro para uma matriz de sinalizadores, cada sinalizador correspondente a uma estrutura [ADRENTRY](adrentry.md) no parâmetro  _lpAdrList,_ que fornece o status da operação de resolução de nomes para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="0c184-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="0c184-128">Os sinalizadores no  _parâmetro lpFlagList_ estão na mesma ordem que as entradas em  _lpAdrList_.</span><span class="sxs-lookup"><span data-stu-id="0c184-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="0c184-129">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="0c184-129">The following flags can be set:</span></span>
    
<span data-ttu-id="0c184-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="0c184-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="0c184-131">O destinatário correspondente foi resolvido, mas não para um identificador de entrada exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0c184-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="0c184-132">Outros contêineres não devem tentar resolver esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="0c184-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="0c184-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="0c184-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="0c184-134">O destinatário correspondente foi resolvido para um identificador de entrada exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0c184-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="0c184-135">Outros contêineres não devem tentar resolver esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="0c184-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="0c184-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="0c184-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="0c184-137">A entrada correspondente não foi resolvida.</span><span class="sxs-lookup"><span data-stu-id="0c184-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="0c184-138">Outros contêineres devem tentar resolver esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="0c184-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c184-139">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0c184-139">Return value</span></span>

<span data-ttu-id="0c184-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c184-140">S_OK</span></span> 
  
> <span data-ttu-id="0c184-141">O processo de resolução de nomes foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0c184-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="0c184-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0c184-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0c184-143">O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="0c184-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="0c184-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0c184-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0c184-145">O provedor de agendas não dá suporte à resolução de nomes em massa usando esse método.</span><span class="sxs-lookup"><span data-stu-id="0c184-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c184-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c184-146">Remarks</span></span>

<span data-ttu-id="0c184-147">O **método ResolveNames** tenta fazer a combinação de destinatários não resolvidos da matriz de entradas no parâmetro  _lpAdrList_ para destinatários neste contêiner de livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="0c184-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="0c184-148">Um destinatário não resolvido normalmente tem apenas a PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e, possivelmente, algumas outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="0c184-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="0c184-149">Um destinatário não resolvido não tem a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), e seu sinalizador correspondente no parâmetro  _lpFlagList_ é definido como MAPI_UNRESOLVED.</span><span class="sxs-lookup"><span data-stu-id="0c184-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="0c184-150">Por outro lado, um destinatário resolvido sempre tem pelo menos a propriedade **PR_ENTRYID,** além de várias outras propriedades, como **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME** e **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0c184-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="0c184-151">A resolução de nomes normalmente começa quando um cliente chama o [método IAddrBook::ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="0c184-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="0c184-152">O MAPI do Outlook responde chamando o método **ResolveNames** de cada contêiner de livro de endereços incluído no caminho de pesquisa do livro de endereços, especificado pela propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0c184-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="0c184-153">As entradas no parâmetro  _lpAdrList_ incluem destinatários já resolvidos porque estão em contêineres para os quais o MAPI já chamou **ResolveNames**, porque as entradas aparecem anteriormente no caminho de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0c184-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="0c184-154">Cada contêiner tenta resolver as entradas não resolvidas, combinando o nome de exibição do destinatário com o nome de exibição de uma de suas entradas.</span><span class="sxs-lookup"><span data-stu-id="0c184-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="0c184-155">Quando uma combinação exclusiva é encontrada, **ResolveNames** adiciona a propriedade **PR_ENTRYID** e outras propriedades incluídas no parâmetro  _lpPropTagArray_ à entrada correspondente na estrutura **ADRLIST** de saída.</span><span class="sxs-lookup"><span data-stu-id="0c184-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="0c184-156">**ResolveNames** define a entrada no parâmetro  _lpFlagList_ como MAPI_RESOLVED.</span><span class="sxs-lookup"><span data-stu-id="0c184-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="0c184-157">O identificador de entrada armazenado **na PR_ENTRYID** propriedade pode ser de curto ou longo prazo.</span><span class="sxs-lookup"><span data-stu-id="0c184-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="0c184-158">Depois que todos os contêineres no caminho de pesquisa tentarem o processo de resolução de nomes, o MAPI abrirá uma caixa de diálogo, se possível, para solicitar ao usuário ajuda na resolução de conflitos restantes.</span><span class="sxs-lookup"><span data-stu-id="0c184-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="0c184-159">Os clientes também podem usar a estrutura **ADRLIST retornada** em chamadas para o [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="0c184-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0c184-160">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="0c184-160">Notes to implementers</span></span>

<span data-ttu-id="0c184-161">Não é necessário dar suporte à resolução de nomes com o **método ResolveNames.**</span><span class="sxs-lookup"><span data-stu-id="0c184-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="0c184-162">Em vez disso, ou adicionalmente, você pode dar suporte a ele com a **restrição de propriedade PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0c184-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="0c184-163">Se você decidir depender da restrição de **PR_ANR** para resolução de nomes, poderá retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="0c184-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="0c184-164">Para obter mais informações, consulte [Implementando a resolução de nomes.](implementing-name-resolution.md)</span><span class="sxs-lookup"><span data-stu-id="0c184-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="0c184-165">Defina a entrada de sinalizador de um destinatário no parâmetro  _lpFlagList_ como MAPI_UNRESOLVED se o destinatário não corresponder a nenhum dos destinatários do contêiner.</span><span class="sxs-lookup"><span data-stu-id="0c184-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="0c184-166">Quando um destinatário corresponde a vários destinatários, de definir seu sinalizador como MAPI_AMBIGUOUS e não alterar sua estrutura **ADRENTRY.**</span><span class="sxs-lookup"><span data-stu-id="0c184-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="0c184-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span><span class="sxs-lookup"><span data-stu-id="0c184-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="0c184-168">Você pode incluí-los na estrutura **ADRENTRY** como parte do processo de resolução de nomes ou aguardar que o MAPI solicite-os com chamadas para os métodos [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) e [IMAPISupport::ExpandRecips.](imapisupport-expandrecips.md)</span><span class="sxs-lookup"><span data-stu-id="0c184-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="0c184-169">Você pode eliminar essas chamadas extras e melhorar o desempenho incluindo as seguintes propriedades nas estruturas **ADRENTRY** de todos os destinatários resolvidos:</span><span class="sxs-lookup"><span data-stu-id="0c184-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="0c184-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="0c184-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="0c184-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="0c184-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="0c184-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="0c184-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="0c184-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="0c184-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="0c184-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c184-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="0c184-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c184-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="0c184-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c184-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="0c184-177">Se algumas das propriedades no parâmetro  _lpPropTagArray_ não estão disponíveis— normalmente porque a entrada do contêiner não dá suporte às propriedades e elas não estão incluídas no membro **ADRENTRY** do destinatário na estrutura **ADRLIST** — defina o tipo de propriedade de cada propriedade indisponível como PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="0c184-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="0c184-178">Não remova nenhuma propriedade da estrutura **ADRENTRY** de um destinatário resolvido.</span><span class="sxs-lookup"><span data-stu-id="0c184-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="0c184-179">Se você deve substituir em vez de modificar uma estrutura **ADRENTRY,** livre a estrutura **ADRENTRY** original primeiro chamando a função [MAPIFreeBuffer](mapifreebuffer.md) e, em seguida, aloque a estrutura **de substituição ADRENTRY** com [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="0c184-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c184-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c184-180">See also</span></span>



[<span data-ttu-id="0c184-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="0c184-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="0c184-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="0c184-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="0c184-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="0c184-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="0c184-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="0c184-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="0c184-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="0c184-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="0c184-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="0c184-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="0c184-187">Propriedade canônica PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="0c184-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="0c184-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="0c184-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="0c184-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0c184-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

