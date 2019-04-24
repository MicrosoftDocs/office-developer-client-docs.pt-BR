---
title: Propriedade canônica PidTagEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328585"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="db1a5-103">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="db1a5-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="db1a5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db1a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db1a5-105">Contém um identificador de entrada MAPI usado para abrir e editar as propriedades de um objeto MAPI específico.</span><span class="sxs-lookup"><span data-stu-id="db1a5-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db1a5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="db1a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db1a5-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="db1a5-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="db1a5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="db1a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db1a5-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="db1a5-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="db1a5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="db1a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="db1a5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="db1a5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="db1a5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="db1a5-112">Area:</span></span>  <br/> |<span data-ttu-id="db1a5-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="db1a5-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db1a5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="db1a5-114">Remarks</span></span>

<span data-ttu-id="db1a5-115">Esta propriedade identifica um objeto de **OpenEntry** para instanciar e fornece acesso a todas as suas propriedades por meio da interface derivada apropriada do **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="db1a5-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="db1a5-116">Essa propriedade é uma das propriedades de endereço base para todos os usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="db1a5-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="db1a5-117">Essa propriedade pode conter um identificador de longo prazo ou de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="db1a5-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="db1a5-118">Os identificadores de curto prazo são mais fáceis e rápidos de construir, mas são limitados em seu escopo e duração, normalmente na sessão atual e na estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="db1a5-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="db1a5-119">Normalmente, eles são usados para objetos de uma natureza temporária, como linhas de tabela ou entradas de caixa de diálogo, e, em seguida, abandonados.</span><span class="sxs-lookup"><span data-stu-id="db1a5-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="db1a5-120">Os identificadores de longo prazo são usados para objetos de uma natureza mais ampla e de longa duração.</span><span class="sxs-lookup"><span data-stu-id="db1a5-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="db1a5-121">Essa propriedade está sempre disponível através do método [IMAPIProp::](imapiprop-getprops.md) GetProps seguindo a primeira chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="db1a5-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="db1a5-122">Alguns provedores de serviços podem torná-lo disponível imediatamente após a instanciação.</span><span class="sxs-lookup"><span data-stu-id="db1a5-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="db1a5-123">O provedor deve sempre retornar um identificador de entrada de longo prazo \*\*\*\* de GetProps.</span><span class="sxs-lookup"><span data-stu-id="db1a5-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="db1a5-124">Portanto, para converter um identificador de curto prazo para longo prazo, basta abrir o objeto e obter sua propriedade por meio de \*\*\*\* GetProps.</span><span class="sxs-lookup"><span data-stu-id="db1a5-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="db1a5-125">A tabela a seguir resume diferenças importantes entre essa propriedade, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="db1a5-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="db1a5-126">**Características**</span><span class="sxs-lookup"><span data-stu-id="db1a5-126">**Characteristic**</span></span>|<span data-ttu-id="db1a5-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="db1a5-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="db1a5-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="db1a5-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="db1a5-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="db1a5-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="db1a5-130">Obrigatório em objetos Attachment</span><span class="sxs-lookup"><span data-stu-id="db1a5-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="db1a5-131">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-131">No</span></span>  <br/> |<span data-ttu-id="db1a5-132">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-132">Yes</span></span>  <br/> |<span data-ttu-id="db1a5-133">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-133">No</span></span>  <br/> |
|<span data-ttu-id="db1a5-134">Obrigatório em objetos Folder</span><span class="sxs-lookup"><span data-stu-id="db1a5-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="db1a5-135">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-135">Yes</span></span>  <br/> |<span data-ttu-id="db1a5-136">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-136">Yes</span></span>  <br/> |<span data-ttu-id="db1a5-137">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-137">No</span></span>  <br/> |
|<span data-ttu-id="db1a5-138">Obrigatório nos objetos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="db1a5-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="db1a5-139">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-139">Yes</span></span>  <br/> |<span data-ttu-id="db1a5-140">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-140">Yes</span></span>  <br/> |<span data-ttu-id="db1a5-141">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-141">No</span></span>  <br/> |
|<span data-ttu-id="db1a5-142">Obrigatório nos objetos status</span><span class="sxs-lookup"><span data-stu-id="db1a5-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="db1a5-143">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-143">Yes</span></span>  <br/> |<span data-ttu-id="db1a5-144">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-144">No</span></span>  <br/> |<span data-ttu-id="db1a5-145">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-145">No</span></span>  <br/> |
|<span data-ttu-id="db1a5-146">Criado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="db1a5-146">Created by client</span></span>  <br/> |<span data-ttu-id="db1a5-147">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-147">No</span></span>  <br/> |<span data-ttu-id="db1a5-148">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-148">No</span></span>  <br/> |<span data-ttu-id="db1a5-149">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-149">Yes</span></span>  <br/> |
|<span data-ttu-id="db1a5-150">Disponível antes da chamada para **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="db1a5-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="db1a5-151">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="db1a5-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="db1a5-152">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="db1a5-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="db1a5-153">Para mensagens, sim.</span><span class="sxs-lookup"><span data-stu-id="db1a5-153">For messages, Yes.</span></span> <span data-ttu-id="db1a5-154">Para outros, depende da implementação do provedor.</span><span class="sxs-lookup"><span data-stu-id="db1a5-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="db1a5-155">Alterado em uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="db1a5-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="db1a5-156">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-156">Yes</span></span>  <br/> |<span data-ttu-id="db1a5-157">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-157">Yes</span></span>  <br/> |<span data-ttu-id="db1a5-158">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-158">No</span></span>  <br/> |
|<span data-ttu-id="db1a5-159">É possível alterar o cliente após uma cópia</span><span class="sxs-lookup"><span data-stu-id="db1a5-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="db1a5-160">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-160">No</span></span>  <br/> |<span data-ttu-id="db1a5-161">Não</span><span class="sxs-lookup"><span data-stu-id="db1a5-161">No</span></span>  <br/> |<span data-ttu-id="db1a5-162">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-162">Yes</span></span>  <br/> |
|<span data-ttu-id="db1a5-163">Exclusivo no</span><span class="sxs-lookup"><span data-stu-id="db1a5-163">Unique within</span></span>  <br/> |<span data-ttu-id="db1a5-164">Todo o mundo</span><span class="sxs-lookup"><span data-stu-id="db1a5-164">Entire world</span></span>  <br/> |<span data-ttu-id="db1a5-165">Instância do provedor</span><span class="sxs-lookup"><span data-stu-id="db1a5-165">Provider instance</span></span>  <br/> |<span data-ttu-id="db1a5-166">Todo o mundo</span><span class="sxs-lookup"><span data-stu-id="db1a5-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="db1a5-167">Binary comparável (como em memcmp)</span><span class="sxs-lookup"><span data-stu-id="db1a5-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="db1a5-168">Não usar [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="db1a5-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="db1a5-169">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-169">Yes</span></span>  <br/> |<span data-ttu-id="db1a5-170">Sim</span><span class="sxs-lookup"><span data-stu-id="db1a5-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="db1a5-171">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="db1a5-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db1a5-172">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="db1a5-172">Protocol specifications</span></span>

<span data-ttu-id="db1a5-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db1a5-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db1a5-174">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="db1a5-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db1a5-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db1a5-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db1a5-176">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="db1a5-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="db1a5-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db1a5-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db1a5-178">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="db1a5-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="db1a5-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db1a5-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db1a5-180">Converte as convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="db1a5-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="db1a5-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db1a5-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db1a5-182">Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="db1a5-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="db1a5-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db1a5-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db1a5-184">Lida com a recuperação de listas de permissões de pastas armazenadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="db1a5-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="db1a5-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db1a5-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db1a5-186">Especifica métodos para conectar e configurar caixas de correio como delegados e interações com objetos de mensagem e calendário quando eles atuam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="db1a5-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="db1a5-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db1a5-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db1a5-188">Especifica o esquema e os métodos usados para solicitar informações de disponibilidade para usuários e recursos.</span><span class="sxs-lookup"><span data-stu-id="db1a5-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db1a5-189">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="db1a5-189">Header files</span></span>

<span data-ttu-id="db1a5-190">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="db1a5-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="db1a5-191">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="db1a5-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="db1a5-192">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="db1a5-192">Mapitags.h</span></span>
  
> <span data-ttu-id="db1a5-193">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="db1a5-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db1a5-194">Confira também</span><span class="sxs-lookup"><span data-stu-id="db1a5-194">See also</span></span>



[<span data-ttu-id="db1a5-195">Propriedade canônica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="db1a5-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="db1a5-196">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="db1a5-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db1a5-197">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="db1a5-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db1a5-198">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="db1a5-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db1a5-199">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="db1a5-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

