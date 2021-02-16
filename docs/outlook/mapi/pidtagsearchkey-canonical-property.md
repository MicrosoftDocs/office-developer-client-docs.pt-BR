---
title: Propriedade canônica PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345462"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="ea23b-103">Propriedade canônica PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="ea23b-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="ea23b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea23b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea23b-105">Contém uma chave binária comparável que identifica objetos correlacionados para uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ea23b-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea23b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ea23b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea23b-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ea23b-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="ea23b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ea23b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea23b-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="ea23b-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="ea23b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ea23b-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea23b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ea23b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ea23b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ea23b-112">Area:</span></span>  <br/> |<span data-ttu-id="ea23b-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="ea23b-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea23b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea23b-114">Remarks</span></span>

<span data-ttu-id="ea23b-115">Essa propriedade fornece um rastreamento para objetos relacionados, como cópias de mensagens, e facilita a localização de ocorrências indesejadas, como destinatários duplicados.</span><span class="sxs-lookup"><span data-stu-id="ea23b-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="ea23b-116">MAPI uses specific rules for constructing search keys for message recipients.</span><span class="sxs-lookup"><span data-stu-id="ea23b-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="ea23b-117">A tecla de pesquisa é formada concatenando o tipo de endereço (em caracteres em maiúsculas), o caractere de dois pontos ':', o endereço de email em formato canônico e o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="ea23b-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="ea23b-118">O formato canônico aqui significa que os endereços com maiúsculas e minúsculas aparecem no caso correto, e os endereços que não são sensíveis a maiúsculas e minúsculas são convertidos em maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="ea23b-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="ea23b-119">Isso é importante para preservar as correlações entre mensagens.</span><span class="sxs-lookup"><span data-stu-id="ea23b-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="ea23b-120">Para objetos de mensagem, essa propriedade está disponível por meio do [método IMAPIProp::GetProps](imapiprop-getprops.md) imediatamente após a criação da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ea23b-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="ea23b-121">Para outros objetos, ele está disponível após a primeira chamada para o [método IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="ea23b-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="ea23b-122">Como essa propriedade é mutável, não é confiável obtendo-la por meio de **GetProps** até que uma chamada **SaveChanges** tenha confirmado valores definidos ou alterados pelo método [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="ea23b-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="ea23b-123">Para perfis, o MAPI também fornece uma seção de perfil em código chamada **MUID_PROFILE_INSTANCE**, com essa propriedade como sua propriedade única.</span><span class="sxs-lookup"><span data-stu-id="ea23b-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="ea23b-124">Essa chave é garantidamente exclusiva entre todos os perfis já criados e pode ser mais confiável do que a propriedade **PR_PROFILE_NAME** ([PidTagProfileName),](pidtagprofilename-canonical-property.md)que pode ser, por exemplo, excluída e recriada com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ea23b-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="ea23b-125">A tabela a seguir resume diferenças importantes entre PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="ea23b-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="ea23b-126">**Característica**</span><span class="sxs-lookup"><span data-stu-id="ea23b-126">**Characteristic**</span></span>|<span data-ttu-id="ea23b-127">PR_ENTRYID\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ea23b-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="ea23b-128">PR_RECORD_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ea23b-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="ea23b-129">PR_SEARCH_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ea23b-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ea23b-130">Obrigatório em objetos anexos</span><span class="sxs-lookup"><span data-stu-id="ea23b-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="ea23b-131">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-131">No</span></span>  <br/> |<span data-ttu-id="ea23b-132">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-132">Yes</span></span>  <br/> |<span data-ttu-id="ea23b-133">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-133">No</span></span>  <br/> |
|<span data-ttu-id="ea23b-134">Obrigatório em objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="ea23b-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="ea23b-135">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-135">Yes</span></span>  <br/> |<span data-ttu-id="ea23b-136">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-136">Yes</span></span>  <br/> |<span data-ttu-id="ea23b-137">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-137">No</span></span>  <br/> |
|<span data-ttu-id="ea23b-138">Obrigatório nos objetos do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="ea23b-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="ea23b-139">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-139">Yes</span></span>  <br/> |<span data-ttu-id="ea23b-140">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-140">Yes</span></span>  <br/> |<span data-ttu-id="ea23b-141">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-141">No</span></span>  <br/> |
|<span data-ttu-id="ea23b-142">Obrigatório em objetos de status</span><span class="sxs-lookup"><span data-stu-id="ea23b-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="ea23b-143">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-143">Yes</span></span>  <br/> |<span data-ttu-id="ea23b-144">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-144">No</span></span>  <br/> |<span data-ttu-id="ea23b-145">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-145">No</span></span>  <br/> |
|<span data-ttu-id="ea23b-146">Criatável pelo cliente</span><span class="sxs-lookup"><span data-stu-id="ea23b-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="ea23b-147">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-147">No</span></span>  <br/> |<span data-ttu-id="ea23b-148">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-148">No</span></span>  <br/> |<span data-ttu-id="ea23b-149">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-149">Yes</span></span>  <br/> |
|<span data-ttu-id="ea23b-150">Disponível antes **de SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="ea23b-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="ea23b-151">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="ea23b-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="ea23b-152">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="ea23b-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="ea23b-153">Para mensagens, Sim.</span><span class="sxs-lookup"><span data-stu-id="ea23b-153">For messages, Yes.</span></span> <span data-ttu-id="ea23b-154">Para outros, depende da implementação do provedor.</span><span class="sxs-lookup"><span data-stu-id="ea23b-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="ea23b-155">Alterado em uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="ea23b-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="ea23b-156">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-156">Yes</span></span>  <br/> |<span data-ttu-id="ea23b-157">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-157">Yes</span></span>  <br/> |<span data-ttu-id="ea23b-158">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-158">No</span></span>  <br/> |
|<span data-ttu-id="ea23b-159">Alterável pelo cliente após uma cópia</span><span class="sxs-lookup"><span data-stu-id="ea23b-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="ea23b-160">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-160">No</span></span>  <br/> |<span data-ttu-id="ea23b-161">Não</span><span class="sxs-lookup"><span data-stu-id="ea23b-161">No</span></span>  <br/> |<span data-ttu-id="ea23b-162">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-162">Yes</span></span>  <br/> |
|<span data-ttu-id="ea23b-163">Exclusivo em ...</span><span class="sxs-lookup"><span data-stu-id="ea23b-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="ea23b-164">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="ea23b-164">Entire world</span></span>  <br/> |<span data-ttu-id="ea23b-165">Instância do provedor</span><span class="sxs-lookup"><span data-stu-id="ea23b-165">Provider instance</span></span>  <br/> |<span data-ttu-id="ea23b-166">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="ea23b-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="ea23b-167">Binário comparável (como com memcmp)</span><span class="sxs-lookup"><span data-stu-id="ea23b-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="ea23b-168">Não -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="ea23b-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="ea23b-169">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-169">Yes</span></span>  <br/> |<span data-ttu-id="ea23b-170">Sim</span><span class="sxs-lookup"><span data-stu-id="ea23b-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ea23b-171">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea23b-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea23b-172">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ea23b-172">Protocol specifications</span></span>

<span data-ttu-id="ea23b-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea23b-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea23b-174">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ea23b-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea23b-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea23b-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea23b-176">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="ea23b-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ea23b-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea23b-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea23b-178">Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="ea23b-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea23b-179">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="ea23b-179">Header files</span></span>

<span data-ttu-id="ea23b-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea23b-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea23b-181">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ea23b-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea23b-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ea23b-182">Mapitags.h</span></span>
  
> <span data-ttu-id="ea23b-183">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ea23b-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea23b-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea23b-184">See also</span></span>



[<span data-ttu-id="ea23b-185">Propriedade canônica PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="ea23b-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="ea23b-186">Propriedade canônica PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="ea23b-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="ea23b-187">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ea23b-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea23b-188">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ea23b-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea23b-189">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ea23b-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea23b-190">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ea23b-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

