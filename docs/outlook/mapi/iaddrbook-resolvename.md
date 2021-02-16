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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408128"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="ef8dd-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="ef8dd-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="ef8dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef8dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef8dd-105">Executa a resolução de nomes, atribuindo identificadores de entrada a destinatários em uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="ef8dd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef8dd-106">Parameters</span></span>

 <span data-ttu-id="ef8dd-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ef8dd-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="ef8dd-108">[in] Um alça para a janela pai de uma caixa de diálogo que é mostrada, se especificada, para solicitar que o usuário resolva a ambiguidade.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="ef8dd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ef8dd-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ef8dd-110">[in] Uma máscara de bits de sinalizadores que controlam vários aspectos do processo de resolução.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="ef8dd-111">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ef8dd-111">The following flags can be set:</span></span>
    
<span data-ttu-id="ef8dd-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="ef8dd-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="ef8dd-113">Indica que  _lpszNewEntryTitle_ é uma cadeia de caracteres UNICODE.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="ef8dd-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="ef8dd-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="ef8dd-115">Use somente o livro de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="ef8dd-116">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="ef8dd-117">Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="ef8dd-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ef8dd-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="ef8dd-119">Exibe uma caixa de diálogo para solicitar ao usuário informações adicionais de resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="ef8dd-120">Se esse sinalizador não estiver definido, nenhuma caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="ef8dd-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ef8dd-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ef8dd-122">Indica que as propriedades retornadas na lista de endereços devem ser do tipo PT_UNICODE em vez de PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="ef8dd-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="ef8dd-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="ef8dd-124">[in] Um ponteiro para o texto do título do controle na caixa de diálogo que solicita que o usuário insira um destinatário.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="ef8dd-125">O título varia dependendo do tipo de destinatário.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="ef8dd-126">O  _parâmetro lpszNewEntryTitle_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ef8dd-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="ef8dd-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="ef8dd-128">[in-out] Um ponteiro para uma [estrutura ADRLIST](adrlist.md) que contém a lista de nomes de destinatários a serem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="ef8dd-129">Essa **estrutura ADRLIST** pode ser criada pelo [método IAddrBook::Address.](iaddrbook-address.md)</span><span class="sxs-lookup"><span data-stu-id="ef8dd-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ef8dd-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ef8dd-130">Return value</span></span>

<span data-ttu-id="ef8dd-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef8dd-131">S_OK</span></span> 
  
> <span data-ttu-id="ef8dd-132">O processo de resolução de nomes foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="ef8dd-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="ef8dd-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="ef8dd-134">Pelo menos um destinatário no parâmetro  _lpAdrList_ corresponderam a mais de uma entrada no livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="ef8dd-135">Normalmente, esse valor é retornado quando o sinalizador MAPI_DIALOG é definido, proibindo a exibição de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="ef8dd-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ef8dd-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ef8dd-137">Pelo menos um destinatário no parâmetro  _lpAdrList_ não pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="ef8dd-138">Normalmente, esse valor é retornado quando o sinalizador MAPI_DIALOG é definido, proibindo a exibição de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ef8dd-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef8dd-139">Remarks</span></span>

<span data-ttu-id="ef8dd-140">Os clientes e provedores de serviços chamam o **método ResolveName** para iniciar o processo de resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="ef8dd-141">Uma entrada não resolvida é uma entrada que ainda não tem um identificador de entrada **ou** uma PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ef8dd-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="ef8dd-142">**ResolveName** passa pelo processo a seguir para cada entrada não resolvida na lista de endereços passada no _parâmetro lpAdrList._</span><span class="sxs-lookup"><span data-stu-id="ef8dd-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="ef8dd-143">Se o tipo de endereço do destinatário aderir ao formato de um endereço SMTP ( _displayname_ @  _domain.top-level-domain_), **ResolveName** atribuirá a ele um identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="ef8dd-144">Para cada contêiner na **propriedade PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** chama o método [IABContainer::ResolveNames.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="ef8dd-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="ef8dd-145">**ResolveNames** tenta corresponder ao nome de exibição de cada destinatário não resolvido com um nome de exibição que pertence a uma de suas entradas.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="ef8dd-146">Se um contêiner não tiver suporte para **ResolveNames,** **ResolveName** restringirá a tabela de conteúdo do contêiner usando uma restrição de propriedade **PR_ANR** ([PidTagAnr).](pidtaganr-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="ef8dd-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="ef8dd-147">Essa restrição faz com que o contêiner execute um tipo de pesquisa de "melhor suposição" para localizar um destinatário correspondente.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="ef8dd-148">Todos os contêineres devem suportar a **restrição PR_ANR** propriedade.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="ef8dd-149">Quando um contêiner retorna um destinatário que corresponde a vários nomes, **ResolveName** exibe uma caixa de diálogo se o sinalizador MAPI_DIALOG estiver definido, o que permite que o usuário selecione o nome correto.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="ef8dd-150">Se todos os contêineres na propriedade **PR_AB_SEARCH_PATH** foram chamados e nenhuma combinação foi encontrada, o destinatário permanece não resolvido.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="ef8dd-151">Se um ou mais destinatários não tiverem resolvido, **ResolveName** retornará MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="ef8dd-152">Se um ou mais destinatários tiveram resolução ambígua que não pôde ser resolvida com uma caixa de diálogo ou porque o sinalizador MAPI_DIALOG não foi definido, **ResolveName** retornará MAPI_E_AMBIGUOUS_RECIP.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="ef8dd-153">Quando alguns dos destinatários são ambíguos e outros não podem ser resolvidos, **ResolveName** pode retornar qualquer um dos valores de erro.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="ef8dd-154">Se um nome não puder ser resolvido, o cliente poderá criar um endereço único que tenha um endereço especialmente formatado e um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="ef8dd-155">Para obter mais informações sobre o formato de identificadores de entrada único, consulte [Identificadores de entrada único.](one-off-entry-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ef8dd-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="ef8dd-156">Para obter mais informações sobre o formato de endereços one-off, consulte [Endereços One-Off.](one-off-addresses.md)</span><span class="sxs-lookup"><span data-stu-id="ef8dd-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="ef8dd-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; se você definir o sinalizador MAPI_UNICODE, as seguintes propriedades serão retornadas como tipos PT_UNICODE estruturas [ADRENTRY:](adrentry.md)</span><span class="sxs-lookup"><span data-stu-id="ef8dd-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="ef8dd-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef8dd-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="ef8dd-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef8dd-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="ef8dd-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef8dd-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="ef8dd-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef8dd-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="ef8dd-162">No entanto, **a PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) é sempre retornada como tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ef8dd-163">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ef8dd-163">MFCMAPI reference</span></span>

<span data-ttu-id="ef8dd-164">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ef8dd-165">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ef8dd-165">**File**</span></span>|<span data-ttu-id="ef8dd-166">**Função**</span><span class="sxs-lookup"><span data-stu-id="ef8dd-166">**Function**</span></span>|<span data-ttu-id="ef8dd-167">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ef8dd-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef8dd-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ef8dd-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ef8dd-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="ef8dd-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="ef8dd-170">MFCMAPI usa o **método ResolveName** para resolver um endereço único antes de adiá-lo a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="ef8dd-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ef8dd-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ef8dd-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="ef8dd-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="ef8dd-173">MFCMAPI usa o **método ResolveName** para procurar uma entrada do livro de endereços por nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="ef8dd-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef8dd-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef8dd-174">See also</span></span>



[<span data-ttu-id="ef8dd-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ef8dd-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="ef8dd-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="ef8dd-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="ef8dd-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="ef8dd-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="ef8dd-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ef8dd-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ef8dd-179">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ef8dd-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

