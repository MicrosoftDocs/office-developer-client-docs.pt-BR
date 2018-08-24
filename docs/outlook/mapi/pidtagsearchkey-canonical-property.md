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
ms.openlocfilehash: da7d19407856570a628529877252360d1537bae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595388"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="cae13-103">Propriedade canônica PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="cae13-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="cae13-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cae13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cae13-105">Contém uma chave binário-comparável que identifica objetos correlatas para uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="cae13-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cae13-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cae13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cae13-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="cae13-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="cae13-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cae13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cae13-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="cae13-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="cae13-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cae13-110">Data type:</span></span>  <br/> |<span data-ttu-id="cae13-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cae13-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cae13-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cae13-112">Area:</span></span>  <br/> |<span data-ttu-id="cae13-113">Propriedades de identificação</span><span class="sxs-lookup"><span data-stu-id="cae13-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cae13-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cae13-114">Remarks</span></span>

<span data-ttu-id="cae13-115">Esta propriedade fornece um rastreamento para objetos relacionados, como cópias da mensagem e facilita a encontrar ocorrências indesejadas, como destinatários duplicados.</span><span class="sxs-lookup"><span data-stu-id="cae13-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="cae13-116">O MAPI usa regras específicas para a construção de chaves de pesquisa para os destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="cae13-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="cae13-117">A chave de pesquisa é formada concatenando o tipo de endereço (em caracteres maiusculos), o caractere de dois-pontos ':', o endereço de email em forma canônica e o caractere de terminação null.</span><span class="sxs-lookup"><span data-stu-id="cae13-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="cae13-118">Forma canônica aqui significa que diferencia maiusculas de minúsculas endereços aparecem em maiusculas e minúsculas, e os endereços que não diferenciam maiusculas de minúsculas são convertidos em maiusculos.</span><span class="sxs-lookup"><span data-stu-id="cae13-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="cae13-119">Isso é importante na preservação correlações entre mensagens.</span><span class="sxs-lookup"><span data-stu-id="cae13-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="cae13-120">Para objetos de mensagem, essa propriedade está disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) imediatamente após a criação da mensagem.</span><span class="sxs-lookup"><span data-stu-id="cae13-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="cae13-121">Para outros objetos, está disponível após a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="cae13-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="cae13-122">Como essa propriedade é podem ser alterada, ele não é confiável obtê-lo por meio de **GetProps** até que uma chamada **SaveChanges** foi confirmada quaisquer valores definidos ou alterados pelo método [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="cae13-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="cae13-123">Para os perfis, MAPI também fornece uma seção de perfil codificadas denominada **MUID_PROFILE_INSTANCE**, com esta propriedade como sua propriedade única.</span><span class="sxs-lookup"><span data-stu-id="cae13-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="cae13-124">Essa chave é garantido que ser exclusivo entre todos os perfis que nunca foi criados e pode ser mais confiável do que a propriedade **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), que pode ser, por exemplo, excluída e recriada com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="cae13-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="cae13-125">A tabela a seguir resume as diferenças importantes entre **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cae13-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="cae13-126">**Característica**</span><span class="sxs-lookup"><span data-stu-id="cae13-126">**Characteristic**</span></span>|<span data-ttu-id="cae13-127">PR_ENTRYID \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cae13-127">****PR_ENTRYID****</span></span>|<span data-ttu-id="cae13-128">PR_RECORD_KEY \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cae13-128">****PR_RECORD_KEY****</span></span>|<span data-ttu-id="cae13-129">PR_SEARCH_KEY \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cae13-129">****PR_SEARCH_KEY****</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cae13-130">Necessários nos objetos attachment</span><span class="sxs-lookup"><span data-stu-id="cae13-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="cae13-131">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-131">No</span></span>  <br/> |<span data-ttu-id="cae13-132">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-132">Yes</span></span>  <br/> |<span data-ttu-id="cae13-133">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-133">No</span></span>  <br/> |
|<span data-ttu-id="cae13-134">Necessários nos objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="cae13-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="cae13-135">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-135">Yes</span></span>  <br/> |<span data-ttu-id="cae13-136">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-136">Yes</span></span>  <br/> |<span data-ttu-id="cae13-137">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-137">No</span></span>  <br/> |
|<span data-ttu-id="cae13-138">Necessários nos objetos de repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="cae13-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="cae13-139">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-139">Yes</span></span>  <br/> |<span data-ttu-id="cae13-140">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-140">Yes</span></span>  <br/> |<span data-ttu-id="cae13-141">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-141">No</span></span>  <br/> |
|<span data-ttu-id="cae13-142">Necessários nos objetos de status</span><span class="sxs-lookup"><span data-stu-id="cae13-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="cae13-143">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-143">Yes</span></span>  <br/> |<span data-ttu-id="cae13-144">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-144">No</span></span>  <br/> |<span data-ttu-id="cae13-145">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-145">No</span></span>  <br/> |
|<span data-ttu-id="cae13-146">Creatable pelo cliente</span><span class="sxs-lookup"><span data-stu-id="cae13-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="cae13-147">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-147">No</span></span>  <br/> |<span data-ttu-id="cae13-148">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-148">No</span></span>  <br/> |<span data-ttu-id="cae13-149">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-149">Yes</span></span>  <br/> |
|<span data-ttu-id="cae13-150">Disponíveis antes **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="cae13-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="cae13-151">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="cae13-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="cae13-152">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="cae13-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="cae13-153">Para mensagens, Sim.</span><span class="sxs-lookup"><span data-stu-id="cae13-153">For messages, Yes.</span></span> <span data-ttu-id="cae13-154">Para outras pessoas, ela depende da implementação do provedor.</span><span class="sxs-lookup"><span data-stu-id="cae13-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="cae13-155">Alterado em uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="cae13-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="cae13-156">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-156">Yes</span></span>  <br/> |<span data-ttu-id="cae13-157">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-157">Yes</span></span>  <br/> |<span data-ttu-id="cae13-158">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-158">No</span></span>  <br/> |
|<span data-ttu-id="cae13-159">Podem ser alterados pelo cliente após uma cópia</span><span class="sxs-lookup"><span data-stu-id="cae13-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="cae13-160">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-160">No</span></span>  <br/> |<span data-ttu-id="cae13-161">Não</span><span class="sxs-lookup"><span data-stu-id="cae13-161">No</span></span>  <br/> |<span data-ttu-id="cae13-162">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-162">Yes</span></span>  <br/> |
|<span data-ttu-id="cae13-163">Unique dentro …</span><span class="sxs-lookup"><span data-stu-id="cae13-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="cae13-164">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="cae13-164">Entire world</span></span>  <br/> |<span data-ttu-id="cae13-165">Instância do provedor</span><span class="sxs-lookup"><span data-stu-id="cae13-165">Provider instance</span></span>  <br/> |<span data-ttu-id="cae13-166">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="cae13-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="cae13-167">Binário comparável (assim como acontece com memcmp)</span><span class="sxs-lookup"><span data-stu-id="cae13-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="cae13-168">Não-- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="cae13-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="cae13-169">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-169">Yes</span></span>  <br/> |<span data-ttu-id="cae13-170">Sim</span><span class="sxs-lookup"><span data-stu-id="cae13-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cae13-171">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cae13-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cae13-172">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cae13-172">Protocol specifications</span></span>

<span data-ttu-id="cae13-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cae13-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cae13-174">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cae13-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cae13-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cae13-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cae13-176">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="cae13-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cae13-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cae13-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cae13-178">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="cae13-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cae13-179">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cae13-179">Header files</span></span>

<span data-ttu-id="cae13-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cae13-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="cae13-181">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cae13-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="cae13-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cae13-182">Mapitags.h</span></span>
  
> <span data-ttu-id="cae13-183">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="cae13-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cae13-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="cae13-184">See also</span></span>



[<span data-ttu-id="cae13-185">Propriedade canônica PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="cae13-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="cae13-186">Propriedade canônica PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="cae13-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="cae13-187">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cae13-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cae13-188">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cae13-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cae13-189">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cae13-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cae13-190">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cae13-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

