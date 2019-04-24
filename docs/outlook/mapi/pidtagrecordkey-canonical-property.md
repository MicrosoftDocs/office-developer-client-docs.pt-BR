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
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="b8fb4-103">Propriedade canônica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="b8fb4-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="b8fb4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8fb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8fb4-105">Contém um identificador equivalente a binário exclusivo para um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8fb4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b8fb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8fb4-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="b8fb4-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="b8fb4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b8fb4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b8fb4-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="b8fb4-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="b8fb4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b8fb4-110">Data type:</span></span>  <br/> |<span data-ttu-id="b8fb4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b8fb4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b8fb4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b8fb4-112">Area:</span></span>  <br/> |<span data-ttu-id="b8fb4-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="b8fb4-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8fb4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8fb4-114">Remarks</span></span>

<span data-ttu-id="b8fb4-115">Essa propriedade facilita a localização de referências a um objeto, como localizar sua linha em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="b8fb4-116">Esta propriedade não pode ser usada para abrir um objeto; Use o identificador de entrada para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="b8fb4-117">Um subobjeto Attachment deve ser identificado exclusivamente dentro de uma mensagem por esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="b8fb4-118">Esse identificador é a única característica de anexo garantida para permanecer a mesma depois que a mensagem é fechada e reaberta.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="b8fb4-119">O provedor de repositório deve preservar essa propriedade nas sessões para garantir essa garantia.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="b8fb4-120">Para pastas, essa propriedade contém uma chave usada na tabela de hierarquia de pastas.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="b8fb4-121">Normalmente, esse é o mesmo valor que o fornecido pela propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b8fb4-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="b8fb4-122">Para repositórios de mensagens, essa propriedade é idêntica à propriedade **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b8fb4-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="b8fb4-123">Em um objeto do repositório de mensagens, essa propriedade deve ser exclusiva em todos os provedores de repositório.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="b8fb4-124">Uma maneira de fazer isso é combinar o valor da propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para o repositório (exclusivo para esse tipo de provedor) com uma estrutura [GUID](guid.md) ou outro valor exclusivo para o repositório de mensagens específico.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="b8fb4-125">Essa propriedade está sempre disponível através do método [IMAPIProp::](imapiprop-getprops.md) GetProps seguindo a primeira chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="b8fb4-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="b8fb4-126">Alguns provedores podem torná-lo disponível imediatamente após a instanciação.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="b8fb4-127">Um cliente ou provedor de serviços pode comparar valores dessa propriedade usando o memcmp.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="b8fb4-128">Isso não é possível para valores de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="b8fb4-129">No enTanto, essa propriedade é segura para ser exclusiva no mesmo contêiner de repositório de mensagens ou de catálogo de endereços; dois objetos de contêineres diferentes podem ter o mesmo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="b8fb4-130">Uma distinção entre o registro e as chaves de pesquisa é que a chave de registro é específica para o objeto, enquanto a chave de pesquisa pode ser copiada para outros objetos.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="b8fb4-131">Por exemplo, duas cópias do objeto podem ter o mesmo valor de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), mas devem ter valores diferentes para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="b8fb4-132">A tabela a seguir resume diferenças importantes entre **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) e essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="b8fb4-133">**Características**</span><span class="sxs-lookup"><span data-stu-id="b8fb4-133">**Characteristic**</span></span>|<span data-ttu-id="b8fb4-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="b8fb4-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="b8fb4-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="b8fb4-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="b8fb4-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="b8fb4-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b8fb4-137">Obrigatório em objetos Attachment</span><span class="sxs-lookup"><span data-stu-id="b8fb4-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="b8fb4-138">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-138">No</span></span>  <br/> |<span data-ttu-id="b8fb4-139">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-139">Yes</span></span>  <br/> |<span data-ttu-id="b8fb4-140">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-140">No</span></span>  <br/> |
|<span data-ttu-id="b8fb4-141">Obrigatório em objetos Folder</span><span class="sxs-lookup"><span data-stu-id="b8fb4-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="b8fb4-142">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-142">Yes</span></span>  <br/> |<span data-ttu-id="b8fb4-143">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-143">Yes</span></span>  <br/> |<span data-ttu-id="b8fb4-144">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-144">No</span></span>  <br/> |
|<span data-ttu-id="b8fb4-145">Obrigatório nos objetos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="b8fb4-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="b8fb4-146">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-146">Yes</span></span>  <br/> |<span data-ttu-id="b8fb4-147">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-147">Yes</span></span>  <br/> |<span data-ttu-id="b8fb4-148">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-148">No</span></span>  <br/> |
|<span data-ttu-id="b8fb4-149">Obrigatório nos objetos status</span><span class="sxs-lookup"><span data-stu-id="b8fb4-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="b8fb4-150">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-150">Yes</span></span>  <br/> |<span data-ttu-id="b8fb4-151">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-151">No</span></span>  <br/> |<span data-ttu-id="b8fb4-152">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-152">No</span></span>  <br/> |
|<span data-ttu-id="b8fb4-153">Criada por cliente</span><span class="sxs-lookup"><span data-stu-id="b8fb4-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="b8fb4-154">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-154">No</span></span>  <br/> |<span data-ttu-id="b8fb4-155">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-155">No</span></span>  <br/> |<span data-ttu-id="b8fb4-156">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-156">Yes</span></span>  <br/> |
|<span data-ttu-id="b8fb4-157">Disponível antes de uma chamada para **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="b8fb4-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="b8fb4-158">Pode</span><span class="sxs-lookup"><span data-stu-id="b8fb4-158">Maybe</span></span>  <br/> |<span data-ttu-id="b8fb4-159">Pode</span><span class="sxs-lookup"><span data-stu-id="b8fb4-159">Maybe</span></span>  <br/> |<span data-ttu-id="b8fb4-160">Mensagens Sim outras pessoas talvez</span><span class="sxs-lookup"><span data-stu-id="b8fb4-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="b8fb4-161">Alterado em uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="b8fb4-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="b8fb4-162">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-162">Yes</span></span>  <br/> |<span data-ttu-id="b8fb4-163">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-163">Yes</span></span>  <br/> |<span data-ttu-id="b8fb4-164">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-164">No</span></span>  <br/> |
|<span data-ttu-id="b8fb4-165">Ser alterado por um cliente após uma cópia</span><span class="sxs-lookup"><span data-stu-id="b8fb4-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="b8fb4-166">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-166">No</span></span>  <br/> |<span data-ttu-id="b8fb4-167">Não</span><span class="sxs-lookup"><span data-stu-id="b8fb4-167">No</span></span>  <br/> |<span data-ttu-id="b8fb4-168">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-168">Yes</span></span>  <br/> |
|<span data-ttu-id="b8fb4-169">Exclusivo em...</span><span class="sxs-lookup"><span data-stu-id="b8fb4-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="b8fb4-170">Todo o mundo</span><span class="sxs-lookup"><span data-stu-id="b8fb4-170">Entire world</span></span>  <br/> |<span data-ttu-id="b8fb4-171">Instância do provedor</span><span class="sxs-lookup"><span data-stu-id="b8fb4-171">Provider instance</span></span>  <br/> |<span data-ttu-id="b8fb4-172">Todo o mundo</span><span class="sxs-lookup"><span data-stu-id="b8fb4-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="b8fb4-173">Binary comparável (como em memcmp)</span><span class="sxs-lookup"><span data-stu-id="b8fb4-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="b8fb4-174">Não--use **IMAPISupport:: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="b8fb4-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="b8fb4-175">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-175">Yes</span></span>  <br/> |<span data-ttu-id="b8fb4-176">Sim</span><span class="sxs-lookup"><span data-stu-id="b8fb4-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b8fb4-177">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8fb4-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8fb4-178">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="b8fb4-178">Protocol specifications</span></span>

<span data-ttu-id="b8fb4-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8fb4-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8fb4-180">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8fb4-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8fb4-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8fb4-182">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b8fb4-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8fb4-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8fb4-184">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8fb4-185">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b8fb4-185">Header files</span></span>

<span data-ttu-id="b8fb4-186">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b8fb4-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8fb4-187">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="b8fb4-188">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b8fb4-188">Mapitags.h</span></span>
  
> <span data-ttu-id="b8fb4-189">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b8fb4-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8fb4-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8fb4-190">See also</span></span>



[<span data-ttu-id="b8fb4-191">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b8fb4-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8fb4-192">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b8fb4-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8fb4-193">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b8fb4-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8fb4-194">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b8fb4-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

