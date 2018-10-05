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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401696"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="9fe0d-103">Propriedade canônica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="9fe0d-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="9fe0d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fe0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fe0d-105">Contém um identificador binário-comparável exclusivo para um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9fe0d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9fe0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9fe0d-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="9fe0d-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="9fe0d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9fe0d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9fe0d-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="9fe0d-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="9fe0d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9fe0d-110">Data type:</span></span>  <br/> |<span data-ttu-id="9fe0d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9fe0d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9fe0d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9fe0d-112">Area:</span></span>  <br/> |<span data-ttu-id="9fe0d-113">Propriedades de identificação</span><span class="sxs-lookup"><span data-stu-id="9fe0d-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fe0d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fe0d-114">Remarks</span></span>

<span data-ttu-id="9fe0d-115">Essa propriedade facilita a localização referências a um objeto, como a localização de sua linha em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="9fe0d-116">Essa propriedade não pode ser usada para abrir um objeto; Use o identificador de entrada para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="9fe0d-117">Um Subobjeto anexo deve ser identificado exclusivamente dentro de uma mensagem por esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="9fe0d-118">Esse identificador é a única característica de anexo garantida que permanecem o mesmo depois que a mensagem é fechada e reabri-lo.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="9fe0d-119">O provedor de armazenamento deve preservar essa propriedade nas sessões para garantir que essa garantia.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="9fe0d-120">Para pastas, essa propriedade contém uma chave usada na tabela de hierarquia de pasta.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="9fe0d-121">Normalmente, isso é o mesmo valor que é fornecida pela propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9fe0d-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="9fe0d-122">Para repositórios de mensagem, essa propriedade é idêntica à propriedade **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9fe0d-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="9fe0d-123">Em um objeto de repositório de mensagem, esta propriedade deve ser exclusiva entre todos os provedores de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="9fe0d-124">Uma maneira de fazer isso é combinar o valor da propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para o repositório (exclusivo desse tipo de provedor) com uma estrutura [GUID](guid.md) ou outro valor exclusivo para o armazenamento de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="9fe0d-125">Essa propriedade sempre está disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) após a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="9fe0d-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="9fe0d-126">Alguns provedores podem disponibilizá-lo imediatamente após instanciação.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="9fe0d-127">Um provedor de cliente ou serviço pode comparar valores dessa propriedade usando memcmp.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="9fe0d-128">Isso não é possível para os valores de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="9fe0d-129">No entanto, essa propriedade é garantida ser exclusivo dentro do mesmo repositório de mensagem ou recipiente; do catálogo de endereços dois objetos dos contêineres diferentes podem ter o mesmo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="9fe0d-130">Uma distinção entre as chaves de registro e de pesquisa é que a chave do registro é específica para o objeto, enquanto a chave de pesquisa pode ser copiada para outros objetos.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="9fe0d-131">Por exemplo, duas cópias do objeto podem ter o mesmo valor de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), mas devem ter valores diferentes para esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="9fe0d-132">A tabela a seguir resume as diferenças importantes entre **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) e essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="9fe0d-133">**Característica**</span><span class="sxs-lookup"><span data-stu-id="9fe0d-133">**Characteristic**</span></span>|<span data-ttu-id="9fe0d-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="9fe0d-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="9fe0d-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="9fe0d-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="9fe0d-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="9fe0d-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9fe0d-137">Necessários nos objetos attachment</span><span class="sxs-lookup"><span data-stu-id="9fe0d-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="9fe0d-138">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-138">No</span></span>  <br/> |<span data-ttu-id="9fe0d-139">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-139">Yes</span></span>  <br/> |<span data-ttu-id="9fe0d-140">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-140">No</span></span>  <br/> |
|<span data-ttu-id="9fe0d-141">Necessários nos objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="9fe0d-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="9fe0d-142">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-142">Yes</span></span>  <br/> |<span data-ttu-id="9fe0d-143">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-143">Yes</span></span>  <br/> |<span data-ttu-id="9fe0d-144">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-144">No</span></span>  <br/> |
|<span data-ttu-id="9fe0d-145">Necessários nos objetos de repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="9fe0d-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="9fe0d-146">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-146">Yes</span></span>  <br/> |<span data-ttu-id="9fe0d-147">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-147">Yes</span></span>  <br/> |<span data-ttu-id="9fe0d-148">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-148">No</span></span>  <br/> |
|<span data-ttu-id="9fe0d-149">Necessários nos objetos de status</span><span class="sxs-lookup"><span data-stu-id="9fe0d-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="9fe0d-150">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-150">Yes</span></span>  <br/> |<span data-ttu-id="9fe0d-151">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-151">No</span></span>  <br/> |<span data-ttu-id="9fe0d-152">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-152">No</span></span>  <br/> |
|<span data-ttu-id="9fe0d-153">Creatable pelo cliente</span><span class="sxs-lookup"><span data-stu-id="9fe0d-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="9fe0d-154">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-154">No</span></span>  <br/> |<span data-ttu-id="9fe0d-155">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-155">No</span></span>  <br/> |<span data-ttu-id="9fe0d-156">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-156">Yes</span></span>  <br/> |
|<span data-ttu-id="9fe0d-157">Disponíveis antes de uma chamada para **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="9fe0d-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="9fe0d-158">Talvez</span><span class="sxs-lookup"><span data-stu-id="9fe0d-158">Maybe</span></span>  <br/> |<span data-ttu-id="9fe0d-159">Talvez</span><span class="sxs-lookup"><span data-stu-id="9fe0d-159">Maybe</span></span>  <br/> |<span data-ttu-id="9fe0d-160">Mensagens de outras pessoas Sim talvez</span><span class="sxs-lookup"><span data-stu-id="9fe0d-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="9fe0d-161">Alterado em uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="9fe0d-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="9fe0d-162">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-162">Yes</span></span>  <br/> |<span data-ttu-id="9fe0d-163">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-163">Yes</span></span>  <br/> |<span data-ttu-id="9fe0d-164">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-164">No</span></span>  <br/> |
|<span data-ttu-id="9fe0d-165">Podem ser alterados por um cliente após uma cópia</span><span class="sxs-lookup"><span data-stu-id="9fe0d-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="9fe0d-166">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-166">No</span></span>  <br/> |<span data-ttu-id="9fe0d-167">Não</span><span class="sxs-lookup"><span data-stu-id="9fe0d-167">No</span></span>  <br/> |<span data-ttu-id="9fe0d-168">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-168">Yes</span></span>  <br/> |
|<span data-ttu-id="9fe0d-169">Unique dentro …</span><span class="sxs-lookup"><span data-stu-id="9fe0d-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="9fe0d-170">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="9fe0d-170">Entire world</span></span>  <br/> |<span data-ttu-id="9fe0d-171">Instância do provedor</span><span class="sxs-lookup"><span data-stu-id="9fe0d-171">Provider instance</span></span>  <br/> |<span data-ttu-id="9fe0d-172">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="9fe0d-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="9fe0d-173">Binário comparável (assim como acontece com memcmp)</span><span class="sxs-lookup"><span data-stu-id="9fe0d-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="9fe0d-174">Não-- use **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="9fe0d-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="9fe0d-175">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-175">Yes</span></span>  <br/> |<span data-ttu-id="9fe0d-176">Sim</span><span class="sxs-lookup"><span data-stu-id="9fe0d-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9fe0d-177">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fe0d-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9fe0d-178">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9fe0d-178">Protocol specifications</span></span>

<span data-ttu-id="9fe0d-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fe0d-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fe0d-180">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9fe0d-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fe0d-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fe0d-182">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9fe0d-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9fe0d-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9fe0d-184">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9fe0d-185">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9fe0d-185">Header files</span></span>

<span data-ttu-id="9fe0d-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9fe0d-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="9fe0d-187">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="9fe0d-188">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9fe0d-188">Mapitags.h</span></span>
  
> <span data-ttu-id="9fe0d-189">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9fe0d-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9fe0d-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fe0d-190">See also</span></span>



[<span data-ttu-id="9fe0d-191">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9fe0d-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9fe0d-192">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9fe0d-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9fe0d-193">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9fe0d-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9fe0d-194">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9fe0d-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

