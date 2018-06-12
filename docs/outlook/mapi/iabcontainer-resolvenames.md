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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ed87a2a6e3232cec492da6be032cf54cd66c3772
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766833"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="dabb6-103">IABContainer:: ResolveNames</span><span class="sxs-lookup"><span data-stu-id="dabb6-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="dabb6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dabb6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dabb6-105">Executa a resolução de nomes para uma ou mais entradas de destinatário.</span><span class="sxs-lookup"><span data-stu-id="dabb6-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="dabb6-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="dabb6-106">Parameters</span></span>

 <span data-ttu-id="dabb6-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="dabb6-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="dabb6-108">[in] Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade descrevendo as propriedades a serem incluídos na estrutura de [ADRLIST](adrlist.md) retornada pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="dabb6-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="dabb6-109">Para solicitar a conjunto de propriedades padrão do provedor, passe NULL no parâmetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="dabb6-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="dabb6-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dabb6-110">_ulFlags_</span></span>
  
> <span data-ttu-id="dabb6-111">[in] Uma bitmask dos sinalizadores que controla o tipo do texto em cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="dabb6-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="dabb6-112">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="dabb6-112">The following flags can be set:</span></span>
    
<span data-ttu-id="dabb6-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="dabb6-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="dabb6-114">Somente as correspondências exatas proxy endereço serão encontradas; correspondências parciais são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="dabb6-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="dabb6-115">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="dabb6-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="dabb6-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="dabb6-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="dabb6-117">Apenas o catálogo de endereços offline será usado para executar a resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="dabb6-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="dabb6-118">Por exemplo, você pode usar esse sinalizador para habilitar um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="dabb6-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="dabb6-119">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="dabb6-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="dabb6-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dabb6-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="dabb6-121">As propriedades de cadeia de caracteres retornada estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="dabb6-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="dabb6-122">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="dabb6-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="dabb6-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="dabb6-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="dabb6-124">[além, out] Na entrada, um ponteiro para uma estrutura **ADRLIST** que contém a lista de destinatários para ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="dabb6-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="dabb6-125">Na saída, um ponteiro para uma estrutura **ADRLIST** que contém os nomes resolvidos.</span><span class="sxs-lookup"><span data-stu-id="dabb6-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="dabb6-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="dabb6-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="dabb6-127">[além, out] Um ponteiro para uma matriz dos sinalizadores, cada sinalizador correspondente em uma estrutura de [ADRENTRY](adrentry.md) no parâmetro _lpAdrList_ , que fornece o status da operação de resolução de nome do destinatário.</span><span class="sxs-lookup"><span data-stu-id="dabb6-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="dabb6-128">Os sinalizadores no parâmetro _lpFlagList_ estão na mesma ordem como as entradas de _lpAdrList_.</span><span class="sxs-lookup"><span data-stu-id="dabb6-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="dabb6-129">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="dabb6-129">The following flags can be set:</span></span>
    
<span data-ttu-id="dabb6-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="dabb6-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="dabb6-131">O destinatário correspondente foi resolvido, mas não a um identificador exclusivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="dabb6-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="dabb6-132">Outros contêineres não devem tentar resolver o destinatário.</span><span class="sxs-lookup"><span data-stu-id="dabb6-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="dabb6-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="dabb6-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="dabb6-134">O destinatário correspondente a um identificador exclusivo de entrada foi resolvido.</span><span class="sxs-lookup"><span data-stu-id="dabb6-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="dabb6-135">Outros contêineres não devem tentar resolver o destinatário.</span><span class="sxs-lookup"><span data-stu-id="dabb6-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="dabb6-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="dabb6-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="dabb6-137">A entrada correspondente não foi resolvida.</span><span class="sxs-lookup"><span data-stu-id="dabb6-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="dabb6-138">Outros contêineres devem tentar resolver o destinatário.</span><span class="sxs-lookup"><span data-stu-id="dabb6-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dabb6-139">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dabb6-139">Return value</span></span>

<span data-ttu-id="dabb6-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="dabb6-140">S_OK</span></span> 
  
> <span data-ttu-id="dabb6-141">O processo de resolução de nomes foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dabb6-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="dabb6-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="dabb6-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="dabb6-143">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="dabb6-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="dabb6-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="dabb6-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="dabb6-145">O provedor de catálogo de endereços não oferece suporte a resolução de nomes em massa usando esse método.</span><span class="sxs-lookup"><span data-stu-id="dabb6-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dabb6-146">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="dabb6-146">Remarks</span></span>

<span data-ttu-id="dabb6-147">O método **ResolveNames** tenta corresponder destinatários não resolvidos da matriz de entradas no parâmetro _lpAdrList_ para destinatários neste contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="dabb6-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="dabb6-148">Um destinatário não resolvido geralmente tem apenas a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e, possivelmente, algumas outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="dabb6-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="dabb6-149">Um destinatário não resolvido não tem a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e seu sinalizador correspondente no parâmetro _lpFlagList_ estiver definido como MAPI_UNRESOLVED.</span><span class="sxs-lookup"><span data-stu-id="dabb6-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="dabb6-150">Por outro lado, um destinatário resolvido sempre possui pelo menos a propriedade **PR_ENTRYID** plus várias outras propriedades como **PR_ADDRTYPE** ([ , **PR_DISPLAY_NAME**e **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dabb6-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="dabb6-151">Resolução de nomes geralmente inicia quando um cliente chama o método [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="dabb6-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="dabb6-152">MAPI do Outlook responde ao chamar o método **ResolveNames** de cada contêiner de catálogo de endereços incluída no caminho de pesquisa de catálogo de endereços, especificado pela propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dabb6-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="dabb6-153">As entradas no parâmetro _lpAdrList_ incluir destinatários já resolvidos porque eles são nos contêineres para o qual MAPI já chamado **ResolveNames**, pois as entradas aparecem anteriormente no caminho de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="dabb6-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="dabb6-154">Cada contêiner tenta resolver as entradas não resolvidas combinando o nome de exibição do destinatário com o nome de exibição de uma das suas entradas.</span><span class="sxs-lookup"><span data-stu-id="dabb6-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="dabb6-155">Quando é encontrada uma correspondência exclusiva, **ResolveNames** adiciona a propriedade **PR_ENTRYID** e outras propriedades que estão incluídas no parâmetro _lpPropTagArray_ para a entrada correspondente na estrutura **ADRLIST** de saída.</span><span class="sxs-lookup"><span data-stu-id="dabb6-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="dabb6-156">**ResolveNames** , em seguida, define a entrada no parâmetro _lpFlagList_ para MAPI_RESOLVED.</span><span class="sxs-lookup"><span data-stu-id="dabb6-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="dabb6-157">O identificador de entrada armazenado na propriedade **PR_ENTRYID** pode ser curto ou longo prazo.</span><span class="sxs-lookup"><span data-stu-id="dabb6-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="dabb6-158">Afinal dos contêineres na pesquisa caminho tentaram o processo de resolução de nome, MAPI abre uma caixa de diálogo, se possível, para solicitar ao usuário para ajudar a resolver conflitos restantes.</span><span class="sxs-lookup"><span data-stu-id="dabb6-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="dabb6-159">Os clientes também podem usar a estrutura **ADRLIST** retornada em chamadas para o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="dabb6-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dabb6-160">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="dabb6-160">Notes to implementers</span></span>

<span data-ttu-id="dabb6-161">Você não é necessárias para dar suporte a resolução de nomes com o método **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="dabb6-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="dabb6-162">Em vez disso, ou Além disso, você pode oferecer suporte com a restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dabb6-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="dabb6-163">Se você decidir contam com a restrição de **PR_ANR** para resolução de nome, você pode retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="dabb6-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="dabb6-164">Para obter mais informações, consulte [Implementando a resolução de nome](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="dabb6-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="dabb6-165">Defina a entrada de sinalizador de um destinatário no parâmetro _lpFlagList_ para MAPI_UNRESOLVED se o destinatário não corresponder a qualquer um dos destinatários do contêiner.</span><span class="sxs-lookup"><span data-stu-id="dabb6-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="dabb6-166">Quando um destinatário corresponde a vários destinatários, defina seu sinalizador para MAPI_AMBIGUOUS e não altere sua estrutura **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="dabb6-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="dabb6-167">MAPI requer determinadas propriedades para os destinatários incluídos na lista de destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="dabb6-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="dabb6-168">Você pode incluí-las na estrutura **ADRENTRY** como parte do processo de resolução de nome ou aguarde MAPI solicitá-los com chamadas para os métodos [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) e [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="dabb6-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="dabb6-169">Você pode eliminar essas chamadas extras e melhorar o desempenho, incluindo as seguintes propriedades nas estruturas **ADRENTRY** de todos os destinatários resolvidos:</span><span class="sxs-lookup"><span data-stu-id="dabb6-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="dabb6-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="dabb6-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="dabb6-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="dabb6-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="dabb6-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="dabb6-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="dabb6-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="dabb6-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="dabb6-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dabb6-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="dabb6-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dabb6-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="dabb6-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dabb6-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="dabb6-177">Se algumas das propriedades no parâmetro _lpPropTagArray_ não estão disponíveis — normalmente porque a entrada de contêiner não dá suporte as propriedades e eles não são incluídos em membro **ADRENTRY** do destinatário na estrutura de **ADRLIST** — Defina o tipo de propriedade de cada propriedade não está disponível como PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="dabb6-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="dabb6-178">Não remova todas as propriedades da estrutura de **ADRENTRY** do destinatário resolvido.</span><span class="sxs-lookup"><span data-stu-id="dabb6-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="dabb6-179">Se você deve substituir em vez de modificar uma estrutura **ADRENTRY** , livre a estrutura original de **ADRENTRY** primeiro por chamar a função de [MAPIFreeBuffer](mapifreebuffer.md) e alocar a estrutura **ADRENTRY** com [de substituição MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="dabb6-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dabb6-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="dabb6-180">See also</span></span>



[<span data-ttu-id="dabb6-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="dabb6-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="dabb6-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="dabb6-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="dabb6-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="dabb6-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="dabb6-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="dabb6-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="dabb6-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="dabb6-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="dabb6-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="dabb6-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="dabb6-187">Propriedade canônico de PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="dabb6-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="dabb6-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="dabb6-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="dabb6-189">IABContainer: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="dabb6-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

