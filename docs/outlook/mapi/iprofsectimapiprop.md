---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344790"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="d3431-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d3431-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="d3431-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3431-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3431-105">Funciona com as propriedades dos objetos seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="d3431-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3431-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d3431-106">Header file:</span></span>  <br/> |<span data-ttu-id="d3431-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="d3431-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="d3431-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="d3431-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="d3431-109">Objetos de seção de perfil</span><span class="sxs-lookup"><span data-stu-id="d3431-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="d3431-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d3431-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3431-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d3431-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="d3431-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="d3431-112">Called by:</span></span>  <br/> |<span data-ttu-id="d3431-113">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="d3431-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="d3431-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="d3431-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d3431-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="d3431-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="d3431-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="d3431-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="d3431-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="d3431-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="d3431-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="d3431-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="d3431-119">Não-Transacted</span><span class="sxs-lookup"><span data-stu-id="d3431-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d3431-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="d3431-120">Vtable order</span></span>

<span data-ttu-id="d3431-121">Esta interface não tem nenhum método exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d3431-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="d3431-122">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="d3431-122">**Required properties**</span></span>|<span data-ttu-id="d3431-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="d3431-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3431-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3431-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3431-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3431-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="d3431-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3431-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d3431-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d3431-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="d3431-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d3431-128">Notes to callers</span></span>

<span data-ttu-id="d3431-129">A interface **IProfSect** não tem nenhum método exclusivo, mas você pode chamar os métodos [IMAPIProp](imapipropiunknown.md) da seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="d3431-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="d3431-130">Há algumas diferenças entre a implementação do **IProfSect** e outras implementações do **IMAPIProp**:</span><span class="sxs-lookup"><span data-stu-id="d3431-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="d3431-131">**IProfSect** não dá suporte a um modelo de transação.</span><span class="sxs-lookup"><span data-stu-id="d3431-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="d3431-132">**IProfSect** não dá suporte a propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="d3431-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="d3431-133">**IProfSect** reserva o intervalo de identificadores 0x67F0 para o 0x67ff para propriedades seguras.</span><span class="sxs-lookup"><span data-stu-id="d3431-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="d3431-134">Não oferecer suporte a um modelo de transação significa que todas as alterações feitas em uma seção de perfil seguindo as chamadas para os métodos [IMAPIProp:: CopyProps](imapiprop-copyprops.md) e [IMAPIProp:: CopyTo](imapiprop-copyto.md) ocorrem imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d3431-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="d3431-135">As chamadas para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) são bem-sucedidas, mas não realmente salvam as alterações.</span><span class="sxs-lookup"><span data-stu-id="d3431-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="d3431-136">Para ser protegido contra alterações que ocorrem prematuramente, os provedores de serviços precisam fazer cópias de suas seções de perfil que são exibidas aos usuários por meio de folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d3431-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="d3431-137">As folhas de propriedades devem funcionar com a cópia, em vez da seção real de perfil.</span><span class="sxs-lookup"><span data-stu-id="d3431-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="d3431-138">Quando o usuário clica no botão **OK** para verificar se as alterações são precisas, as alterações podem ser salvas na seção perfil real.</span><span class="sxs-lookup"><span data-stu-id="d3431-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="d3431-139">Para implementar uma folha de propriedades usando uma seção de perfil copiada, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="d3431-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="d3431-140">Abra a seção perfil chamando o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) ou [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="d3431-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="d3431-141">Chame a função [CreateIProp](createiprop.md) para recuperar um objeto de dados de propriedade — um objeto que oferece suporte à interface **IPropData** .</span><span class="sxs-lookup"><span data-stu-id="d3431-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="d3431-142">Chame o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) da seção de perfil para copiar as propriedades que serão exibidas na folha de propriedades da seção perfil para o objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d3431-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="d3431-143">Chame o método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para solicitar que o provedor de serviços exiba uma folha de propriedades e passe um ponteiro para o objeto de dados de propriedade no parâmetro _lpConfigData_ .</span><span class="sxs-lookup"><span data-stu-id="d3431-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="d3431-144">Quando o usuário salva as alterações nas propriedades de configuração na folha de propriedades, chame o método [IMAPIProp:: CopyTo](imapiprop-copyto.md) para copiar as propriedades do objeto de dados de propriedade de volta para a seção perfil.</span><span class="sxs-lookup"><span data-stu-id="d3431-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="d3431-145">Seções de perfil, ao contrário de outros objetos, não dão suporte a propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="d3431-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="d3431-146">Os métodos [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp:: GETNAMESFROMIDS](imapiprop-getnamesfromids.md) retornam MAPI_E_NO_SUPPORT se forem chamados em um objeto section de perfil.</span><span class="sxs-lookup"><span data-stu-id="d3431-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="d3431-147">Se você usar o método [IMAPIProp::](imapiprop-setprops.md) SetProps para definir identificadores de propriedade no intervalo acima de 0x8000, o tipo de propriedade PT_ERROR será retornado.</span><span class="sxs-lookup"><span data-stu-id="d3431-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="d3431-148">Seções de perfil Reserve o intervalo de identificadores 0x67F0 para 0x67FF para propriedades seguras.</span><span class="sxs-lookup"><span data-stu-id="d3431-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="d3431-149">Os provedores de serviços podem usar esse intervalo para armazenar senhas e outras credenciais específicas do provedor.</span><span class="sxs-lookup"><span data-stu-id="d3431-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="d3431-150">As propriedades neste intervalo não são retornadas na lista completa de propriedades quando NULL é passado no parâmetro _lpPropTag_ do método [IMAPIProp::](imapiprop-getprops.md) GetProps, nem são retornados no parâmetro _lppPropTagArray_ do [ Método IMAPIProp::](imapiprop-getproplist.md) Getproplist.</span><span class="sxs-lookup"><span data-stu-id="d3431-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="d3431-151">As propriedades seguras devem ser solicitadas especificamente por seus identificadores.</span><span class="sxs-lookup"><span data-stu-id="d3431-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="d3431-152">O MAPI fornece uma seção de perfil com a constante codificada MUID_PROFILE_INSTANCE como seu identificador e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) como sua única propriedade.</span><span class="sxs-lookup"><span data-stu-id="d3431-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="d3431-153">O MAPI garante que o valor da propriedade **PR_SEARCH_KEY** será exclusivo entre todos os perfis criados.</span><span class="sxs-lookup"><span data-stu-id="d3431-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="d3431-154">Use **PR_SEARCH_KEY** em vez de **PR_PROFILE_NAME** quando a exclusividade for importante, pois é possível que um perfil excluído seja seguido por outro perfil com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="d3431-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="d3431-155">Para obter mais informações sobre como usar seções de perfil, consulte [Administração de perfis e serviços de mensagens](administering-profiles-and-message-services.md).</span><span class="sxs-lookup"><span data-stu-id="d3431-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3431-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3431-156">See also</span></span>



[<span data-ttu-id="d3431-157">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="d3431-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

