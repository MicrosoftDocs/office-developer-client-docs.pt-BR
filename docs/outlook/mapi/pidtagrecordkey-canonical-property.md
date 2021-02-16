---
title: Propriedade canônica PidTagRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355262"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="e9b70-103">Propriedade canônica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="e9b70-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="e9b70-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9b70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9b70-105">Contém um identificador binário exclusivo comparável para um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="e9b70-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9b70-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e9b70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9b70-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="e9b70-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="e9b70-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e9b70-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9b70-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="e9b70-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="e9b70-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e9b70-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9b70-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9b70-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9b70-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e9b70-112">Area:</span></span>  <br/> |<span data-ttu-id="e9b70-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="e9b70-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9b70-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9b70-114">Remarks</span></span>

<span data-ttu-id="e9b70-115">Essa propriedade facilita a localização de referências a um objeto, como localizar sua linha em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e9b70-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="e9b70-116">Essa propriedade não pode ser usada para abrir um objeto; use o identificador de entrada para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="e9b70-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="e9b70-117">Um subobjeto de anexo deve ser identificado exclusivamente dentro de uma mensagem por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b70-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="e9b70-118">Esse identificador é a única característica de anexo garantida que se manterá a mesma depois que a mensagem for fechada e reaberta.</span><span class="sxs-lookup"><span data-stu-id="e9b70-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="e9b70-119">O provedor de armazenamento deve preservar essa propriedade entre sessões para garantir essa garantia.</span><span class="sxs-lookup"><span data-stu-id="e9b70-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="e9b70-120">Para pastas, essa propriedade contém uma chave usada na tabela de hierarquia de pastas.</span><span class="sxs-lookup"><span data-stu-id="e9b70-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="e9b70-121">Normalmente, esse é o mesmo valor fornecido pela propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e9b70-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e9b70-122">Para repositórios de mensagens, essa propriedade é idêntica à **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="e9b70-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e9b70-123">Em um objeto de armazenamento de mensagens, essa propriedade deve ser exclusiva em todos os provedores de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e9b70-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="e9b70-124">Uma maneira de fazer isso é combinar o valor da propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para o repositório (exclusivo para esse tipo de provedor) com uma estrutura [GUID](guid.md) ou outro valor exclusivo para o repositório de mensagens específico.</span><span class="sxs-lookup"><span data-stu-id="e9b70-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="e9b70-125">Essa propriedade está sempre disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) após a primeira chamada para o método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="e9b70-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="e9b70-126">Alguns provedores podem torná-lo disponível imediatamente após a instaciação.</span><span class="sxs-lookup"><span data-stu-id="e9b70-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="e9b70-127">Um cliente ou provedor de serviços pode comparar valores dessa propriedade usando o memcmp.</span><span class="sxs-lookup"><span data-stu-id="e9b70-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="e9b70-128">Isso não é possível para valores de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e9b70-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="e9b70-129">No entanto, essa propriedade é garantida como exclusiva dentro do mesmo armazenamento de mensagens ou contêiner do livro de endereços; dois objetos de contêineres diferentes podem ter o mesmo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b70-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="e9b70-130">Uma distinção entre o registro e as teclas de pesquisa é que a chave de registro é específica para o objeto, enquanto a chave de pesquisa pode ser copiada para outros objetos.</span><span class="sxs-lookup"><span data-stu-id="e9b70-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="e9b70-131">Por exemplo, duas cópias do objeto podem ter o mesmo **valor PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), mas devem ter valores diferentes para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b70-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="e9b70-132">A tabela a seguir resume diferenças importantes **entre PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) e esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9b70-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="e9b70-133">**Característica**</span><span class="sxs-lookup"><span data-stu-id="e9b70-133">**Characteristic**</span></span>|<span data-ttu-id="e9b70-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="e9b70-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="e9b70-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="e9b70-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="e9b70-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="e9b70-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e9b70-137">Obrigatório em objetos anexos</span><span class="sxs-lookup"><span data-stu-id="e9b70-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="e9b70-138">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-138">No</span></span>  <br/> |<span data-ttu-id="e9b70-139">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-139">Yes</span></span>  <br/> |<span data-ttu-id="e9b70-140">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-140">No</span></span>  <br/> |
|<span data-ttu-id="e9b70-141">Obrigatório em objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="e9b70-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="e9b70-142">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-142">Yes</span></span>  <br/> |<span data-ttu-id="e9b70-143">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-143">Yes</span></span>  <br/> |<span data-ttu-id="e9b70-144">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-144">No</span></span>  <br/> |
|<span data-ttu-id="e9b70-145">Obrigatório nos objetos do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="e9b70-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="e9b70-146">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-146">Yes</span></span>  <br/> |<span data-ttu-id="e9b70-147">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-147">Yes</span></span>  <br/> |<span data-ttu-id="e9b70-148">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-148">No</span></span>  <br/> |
|<span data-ttu-id="e9b70-149">Obrigatório em objetos de status</span><span class="sxs-lookup"><span data-stu-id="e9b70-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="e9b70-150">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-150">Yes</span></span>  <br/> |<span data-ttu-id="e9b70-151">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-151">No</span></span>  <br/> |<span data-ttu-id="e9b70-152">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-152">No</span></span>  <br/> |
|<span data-ttu-id="e9b70-153">Criatável pelo cliente</span><span class="sxs-lookup"><span data-stu-id="e9b70-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="e9b70-154">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-154">No</span></span>  <br/> |<span data-ttu-id="e9b70-155">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-155">No</span></span>  <br/> |<span data-ttu-id="e9b70-156">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-156">Yes</span></span>  <br/> |
|<span data-ttu-id="e9b70-157">Disponível antes de uma chamada para **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="e9b70-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="e9b70-158">Talvez</span><span class="sxs-lookup"><span data-stu-id="e9b70-158">Maybe</span></span>  <br/> |<span data-ttu-id="e9b70-159">Talvez</span><span class="sxs-lookup"><span data-stu-id="e9b70-159">Maybe</span></span>  <br/> |<span data-ttu-id="e9b70-160">Mensagens Sim, Outras Talvez</span><span class="sxs-lookup"><span data-stu-id="e9b70-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="e9b70-161">Alterado em uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="e9b70-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="e9b70-162">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-162">Yes</span></span>  <br/> |<span data-ttu-id="e9b70-163">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-163">Yes</span></span>  <br/> |<span data-ttu-id="e9b70-164">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-164">No</span></span>  <br/> |
|<span data-ttu-id="e9b70-165">Alterável por um cliente após uma cópia</span><span class="sxs-lookup"><span data-stu-id="e9b70-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="e9b70-166">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-166">No</span></span>  <br/> |<span data-ttu-id="e9b70-167">Não</span><span class="sxs-lookup"><span data-stu-id="e9b70-167">No</span></span>  <br/> |<span data-ttu-id="e9b70-168">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-168">Yes</span></span>  <br/> |
|<span data-ttu-id="e9b70-169">Exclusivo em ...</span><span class="sxs-lookup"><span data-stu-id="e9b70-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="e9b70-170">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="e9b70-170">Entire world</span></span>  <br/> |<span data-ttu-id="e9b70-171">Instância do provedor</span><span class="sxs-lookup"><span data-stu-id="e9b70-171">Provider instance</span></span>  <br/> |<span data-ttu-id="e9b70-172">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="e9b70-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="e9b70-173">Binário comparável (como com memcmp)</span><span class="sxs-lookup"><span data-stu-id="e9b70-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="e9b70-174">Não -- use **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="e9b70-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="e9b70-175">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-175">Yes</span></span>  <br/> |<span data-ttu-id="e9b70-176">Sim</span><span class="sxs-lookup"><span data-stu-id="e9b70-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e9b70-177">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9b70-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9b70-178">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e9b70-178">Protocol specifications</span></span>

<span data-ttu-id="e9b70-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9b70-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9b70-180">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e9b70-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9b70-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9b70-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9b70-182">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="e9b70-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e9b70-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9b70-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9b70-184">Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="e9b70-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9b70-185">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="e9b70-185">Header files</span></span>

<span data-ttu-id="e9b70-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9b70-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9b70-187">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e9b70-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9b70-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9b70-188">Mapitags.h</span></span>
  
> <span data-ttu-id="e9b70-189">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e9b70-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9b70-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9b70-190">See also</span></span>



[<span data-ttu-id="e9b70-191">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e9b70-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9b70-192">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e9b70-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9b70-193">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e9b70-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9b70-194">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e9b70-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

