---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287004"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="30ba4-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="30ba4-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="30ba4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30ba4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30ba4-105">Realiza a resolução de nomes, atribuindo identificadores de entrada a destinatários em uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="30ba4-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="30ba4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30ba4-106">Parameters</span></span>

 <span data-ttu-id="30ba4-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="30ba4-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="30ba4-108">no Uma alça para a janela pai de uma caixa de diálogo exibida, se especificada, para solicitar que o usuário resolva a ambigüidade.</span><span class="sxs-lookup"><span data-stu-id="30ba4-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="30ba4-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="30ba4-109">_ulFlags_</span></span>
  
> <span data-ttu-id="30ba4-110">no Uma bitmask de sinalizadores que controlam vários aspectos do processo de resolução.</span><span class="sxs-lookup"><span data-stu-id="30ba4-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="30ba4-111">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="30ba4-111">The following flags can be set:</span></span>
    
<span data-ttu-id="30ba4-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="30ba4-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="30ba4-113">Indica que _lpszNewEntryTitle_ é uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="30ba4-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="30ba4-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="30ba4-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="30ba4-115">Use apenas o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="30ba4-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="30ba4-116">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="30ba4-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="30ba4-117">Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="30ba4-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="30ba4-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="30ba4-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="30ba4-119">Exibe uma caixa de diálogo para solicitar ao usuário informações de resolução de nome adicionais.</span><span class="sxs-lookup"><span data-stu-id="30ba4-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="30ba4-120">Se esse sinalizador não for definido, nenhuma caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="30ba4-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="30ba4-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="30ba4-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="30ba4-122">Indica que as propriedades retornadas na lista de endereços devem ser do tipo PT_UNICODE em vez de PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="30ba4-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="30ba4-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="30ba4-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="30ba4-124">no Um ponteiro para o texto do título do controle na caixa de diálogo que solicita que o usuário insira um destinatário.</span><span class="sxs-lookup"><span data-stu-id="30ba4-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="30ba4-125">O título varia dependendo do tipo de destinatário.</span><span class="sxs-lookup"><span data-stu-id="30ba4-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="30ba4-126">O parâmetro _lpszNewEntryTitle_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="30ba4-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="30ba4-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="30ba4-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="30ba4-128">[in-out] Um ponteiro para uma estrutura [das ADRLIST](adrlist.md) que contém a lista de nomes de destinatários a serem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="30ba4-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="30ba4-129">Essa estrutura **das ADRLIST** pode ser criada pelo método [IAddrBook:: address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="30ba4-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="30ba4-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="30ba4-130">Return value</span></span>

<span data-ttu-id="30ba4-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="30ba4-131">S_OK</span></span> 
  
> <span data-ttu-id="30ba4-132">O processo de resolução de nomes foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="30ba4-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="30ba4-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="30ba4-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="30ba4-134">Pelo menos um destinatário no parâmetro _lpAdrList_ corresponde a mais de uma entrada no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="30ba4-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="30ba4-135">Normalmente, esse valor é retornado quando o sinalizador MAPI_DIALOG é definido, proibindo a exibição de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="30ba4-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="30ba4-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="30ba4-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="30ba4-137">Pelo menos um destinatário no parâmetro _lpAdrList_ não pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="30ba4-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="30ba4-138">Normalmente, esse valor é retornado quando o sinalizador MAPI_DIALOG é definido, proibindo a exibição de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="30ba4-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="30ba4-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="30ba4-139">Remarks</span></span>

<span data-ttu-id="30ba4-140">Os clientes e os provedores de \*\*\*\* serviços chamam o método ResolveName para iniciar o processo de resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="30ba4-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="30ba4-141">Uma entrada não resolvida é uma entrada que ainda não tem um identificador de entrada ou uma propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="30ba4-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="30ba4-142">\*\*\*\* O resolvedor passa pelo processo a seguir para cada entrada não resolvida na lista de endereços passada no parâmetro _lpAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="30ba4-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="30ba4-143">Se o tipo de endereço do destinatário aderir ao formato de um endereço SMTP (domínio _DisplayName_@ _. Top-Level-Domain_), ResolveName \*\*\*\* atribui um identificador de entrada one-off.</span><span class="sxs-lookup"><span data-stu-id="30ba4-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="30ba4-144">Para cada contêiner na propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** chama o método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="30ba4-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="30ba4-145">**ResolveNames** tenta corresponder o nome de exibição de cada destinatário não resolvido com um nome de exibição que pertença a uma de suas entradas.</span><span class="sxs-lookup"><span data-stu-id="30ba4-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="30ba4-146">Se um contêiner não oferecer suporte \*\*\*\* a ResolveNames, **ResolveName** restringirá a tabela de conteúdo do contêiner usando uma restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="30ba4-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="30ba4-147">Essa restrição faz com que o contêiner realize um tipo de "melhor palpite" de pesquisa para localizar um destinatário correspondente.</span><span class="sxs-lookup"><span data-stu-id="30ba4-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="30ba4-148">Todos os contêineres devem oferecer suporte à restrição de propriedade **PR_ANR** .</span><span class="sxs-lookup"><span data-stu-id="30ba4-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="30ba4-149">Quando um contêiner retorna um destinatário que corresponde a vários nomes \*\*\*\* , ResolveName exibe uma caixa de diálogo se o sinalizador MAPI_DIALOG estiver definido, o que permite ao usuário selecionar o nome correto.</span><span class="sxs-lookup"><span data-stu-id="30ba4-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="30ba4-150">Se todos os contêineres da propriedade **PR_AB_SEARCH_PATH** tiverem sido chamados e se nenhuma correspondência for encontrada, o destinatário permanecerá não resolvido.</span><span class="sxs-lookup"><span data-stu-id="30ba4-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="30ba4-151">Se um ou mais destinatários não forem resolvidos, **ResolveName** retornará MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="30ba4-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="30ba4-152">Se um ou mais destinatários tinham uma resolução ambígua que não pôde ser resolvida com uma caixa de diálogo ou porque o sinalizador MAPI_DIALOG não foi \*\*\*\* definido, ResolveName retorna MAPI_E_AMBIGUOUS_RECIP.</span><span class="sxs-lookup"><span data-stu-id="30ba4-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="30ba4-153">Quando alguns dos destinatários são ambíguos e alguns não podem ser resolvidos, **ResolveName** pode retornar um valor de erro.</span><span class="sxs-lookup"><span data-stu-id="30ba4-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="30ba4-154">Se não for possível resolver um nome, o cliente poderá criar um endereço de one-off que tenha um endereço e um identificador de entrada especialmente formatados.</span><span class="sxs-lookup"><span data-stu-id="30ba4-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="30ba4-155">Para obter mais informações sobre o formato de identificadores de entrada únicos, consulte [identificadores de entrada one-off](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="30ba4-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="30ba4-156">Para obter mais informações sobre o formato de endereços únicos, consulte [endereços one-off](one-off-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="30ba4-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="30ba4-157">O MAPI oferece suporte a cadeias de caracteres Unicode para o **das ADRLIST** e os novos parâmetros de título de entrada para **resolver**; Se você definir o sinalizador MAPI_UNICODE, as seguintes propriedades serão retornadas como tipo PT_UNICODE nas estruturas [ADRENTRY](adrentry.md) :</span><span class="sxs-lookup"><span data-stu-id="30ba4-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="30ba4-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30ba4-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="30ba4-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30ba4-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="30ba4-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30ba4-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="30ba4-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="30ba4-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="30ba4-162">No enTanto, a propriedade **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) é sempre retornada como tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="30ba4-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="30ba4-163">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="30ba4-163">MFCMAPI reference</span></span>

<span data-ttu-id="30ba4-164">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="30ba4-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="30ba4-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="30ba4-165">**File**</span></span>|<span data-ttu-id="30ba4-166">**Função**</span><span class="sxs-lookup"><span data-stu-id="30ba4-166">**Function**</span></span>|<span data-ttu-id="30ba4-167">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="30ba4-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30ba4-168">MAPIABFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="30ba4-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="30ba4-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="30ba4-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="30ba4-170">MFCMAPI usa o \*\*\*\* método ResolveName para resolver um endereço one-off antes de adicioná-lo a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="30ba4-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="30ba4-171">MAPIABFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="30ba4-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="30ba4-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="30ba4-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="30ba4-173">MFCMAPI usa o \*\*\*\* método ResolveName para procurar uma entrada do catálogo de endereços por nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="30ba4-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30ba4-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="30ba4-174">See also</span></span>



[<span data-ttu-id="30ba4-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="30ba4-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="30ba4-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="30ba4-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="30ba4-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="30ba4-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="30ba4-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="30ba4-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="30ba4-179">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="30ba4-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

