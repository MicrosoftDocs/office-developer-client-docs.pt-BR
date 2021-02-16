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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406595"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="768e8-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="768e8-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="768e8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="768e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="768e8-105">Funciona com as propriedades dos objetos de seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="768e8-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="768e8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="768e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="768e8-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="768e8-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="768e8-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="768e8-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="768e8-109">Objetos de seção de perfil</span><span class="sxs-lookup"><span data-stu-id="768e8-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="768e8-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="768e8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="768e8-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="768e8-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="768e8-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="768e8-112">Called by:</span></span>  <br/> |<span data-ttu-id="768e8-113">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="768e8-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="768e8-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="768e8-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="768e8-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="768e8-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="768e8-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="768e8-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="768e8-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="768e8-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="768e8-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="768e8-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="768e8-119">Não traduzido</span><span class="sxs-lookup"><span data-stu-id="768e8-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="768e8-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="768e8-120">Vtable order</span></span>

<span data-ttu-id="768e8-121">Essa interface não tem métodos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="768e8-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="768e8-122">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="768e8-122">**Required properties**</span></span>|<span data-ttu-id="768e8-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="768e8-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="768e8-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="768e8-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="768e8-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="768e8-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="768e8-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="768e8-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="768e8-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="768e8-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="768e8-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="768e8-128">Notes to callers</span></span>

<span data-ttu-id="768e8-129">A interface **IProfSect** não tem métodos exclusivos, mas você pode chamar os métodos [IMAPIProp](imapipropiunknown.md) da seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="768e8-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="768e8-130">Existem algumas diferenças entre a implementação **de IProfSect** e outras implementações de **IMAPIProp**:</span><span class="sxs-lookup"><span data-stu-id="768e8-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="768e8-131">**O IProfSect** não dá suporte a um modelo de transação.</span><span class="sxs-lookup"><span data-stu-id="768e8-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="768e8-132">**O IProfSect não** dá suporte a propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="768e8-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="768e8-133">**O IProfSect** reserva o intervalo de 0x67F0 para 0x67ff propriedades seguras.</span><span class="sxs-lookup"><span data-stu-id="768e8-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="768e8-134">Não oferecer suporte a um modelo de transação significa que todas as alterações feitas em uma seção de perfil após chamadas para os métodos [IMAPIProp::CopyProps](imapiprop-copyprops.md) e [IMAPIProp::CopyTo](imapiprop-copyto.md) ocorrem imediatamente.</span><span class="sxs-lookup"><span data-stu-id="768e8-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="768e8-135">As chamadas para [o método IMAPIProp::SaveChanges](imapiprop-savechanges.md) são bem-sucedidas, mas não salvam alterações.</span><span class="sxs-lookup"><span data-stu-id="768e8-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="768e8-136">Para serem protegidos contra alterações que ocorrem prematuramente, os provedores de serviços precisam fazer cópias de suas seções de perfil que são exibidas para os usuários por meio de folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="768e8-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="768e8-137">As folhas de propriedades devem funcionar com a cópia, em vez da seção de perfil real.</span><span class="sxs-lookup"><span data-stu-id="768e8-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="768e8-138">Quando o usuário clica no **botão OK** para verificar se as alterações são precisas, as alterações podem ser salvas na seção de perfil real.</span><span class="sxs-lookup"><span data-stu-id="768e8-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="768e8-139">Para implementar uma folha de propriedades usando uma seção de perfil copiada, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="768e8-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="768e8-140">Abra a seção de perfil chamando o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="768e8-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="768e8-141">Chame a [função CreateIProp](createiprop.md) para recuperar um objeto de dados de propriedade — um objeto que dá suporte à interface **IPropData.**</span><span class="sxs-lookup"><span data-stu-id="768e8-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="768e8-142">Chame o método [IMAPIProp::CopyTo](imapiprop-copyto.md) da seção de perfil para copiar as propriedades que aparecerão na folha de propriedades da seção de perfil para o objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="768e8-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="768e8-143">Chame o método [IMAPISupport::D oConfigPropSheet](imapisupport-doconfigpropsheet.md) para solicitar que o provedor de serviços exiba uma folha de propriedades e passe um ponteiro para o objeto de dados de propriedade no parâmetro _lpConfigData._</span><span class="sxs-lookup"><span data-stu-id="768e8-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="768e8-144">Quando o usuário salvar as alterações nas propriedades de configuração na folha de propriedades, chame o método [IMAPIProp::CopyTo](imapiprop-copyto.md) para copiar as propriedades do objeto de dados de propriedade de volta para a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="768e8-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="768e8-145">As seções de perfil, ao contrário de outros objetos, não são suportadas por propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="768e8-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="768e8-146">Os [métodos IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) retornam MAPI_E_NO_SUPPORT se eles são chamados em um objeto de seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="768e8-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="768e8-147">Se você usar o método [IMAPIProp::SetProps](imapiprop-setprops.md) para definir identificadores de propriedade no intervalo acima 0x8000, o tipo PT_ERROR propriedade será retornado.</span><span class="sxs-lookup"><span data-stu-id="768e8-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="768e8-148">As seções de perfil reservam o intervalo 0x67F0 identificador para 0x67FF propriedades seguras.</span><span class="sxs-lookup"><span data-stu-id="768e8-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="768e8-149">Os provedores de serviços podem usar esse intervalo para armazenar senhas e outras credenciais específicas do provedor.</span><span class="sxs-lookup"><span data-stu-id="768e8-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="768e8-150">As propriedades nesse intervalo não são retornadas na lista completa de propriedades quando NULL é passado no parâmetro _lpPropTag_ do método [IMAPIProp::GetProps,](imapiprop-getprops.md) nem são retornadas no parâmetro _lppPropTagArray_ do método [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="768e8-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="768e8-151">As propriedades seguras devem ser solicitadas especificamente por seus identificadores.</span><span class="sxs-lookup"><span data-stu-id="768e8-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="768e8-152">O MAPI fornece uma seção de perfil com a constante em código MUID_PROFILE_INSTANCE como seu identificador e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) como sua propriedade única.</span><span class="sxs-lookup"><span data-stu-id="768e8-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="768e8-153">O MAPI garante que o **valor PR_SEARCH_KEY** propriedade será exclusivo entre todos os perfis criados.</span><span class="sxs-lookup"><span data-stu-id="768e8-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="768e8-154">Use **PR_SEARCH_KEY** em vez **de PR_PROFILE_NAME** quando a exclusividade for importante, porque é possível que um perfil excluído seja seguido por outro perfil com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="768e8-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="768e8-155">Para obter mais informações sobre como usar seções de perfil, consulte [Administrando perfis e serviços de mensagens.](administering-profiles-and-message-services.md)</span><span class="sxs-lookup"><span data-stu-id="768e8-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="768e8-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="768e8-156">See also</span></span>



[<span data-ttu-id="768e8-157">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="768e8-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

