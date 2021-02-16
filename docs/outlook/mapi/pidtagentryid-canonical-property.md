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
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="98025-103">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="98025-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="98025-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98025-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98025-105">Contém um identificador de entrada MAPI usado para abrir e editar propriedades de um objeto MAPI específico.</span><span class="sxs-lookup"><span data-stu-id="98025-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98025-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="98025-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98025-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="98025-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="98025-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="98025-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98025-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="98025-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="98025-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="98025-110">Data type:</span></span>  <br/> |<span data-ttu-id="98025-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="98025-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="98025-112">Área:</span><span class="sxs-lookup"><span data-stu-id="98025-112">Area:</span></span>  <br/> |<span data-ttu-id="98025-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="98025-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98025-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="98025-114">Remarks</span></span>

<span data-ttu-id="98025-115">Essa propriedade identifica um objeto para **OpenEntry** in instantiate e fornece acesso a todas as suas propriedades por meio da interface derivada apropriada de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="98025-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="98025-116">Essa propriedade é uma das propriedades de endereço base para todos os usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="98025-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="98025-117">Essa propriedade pode conter um identificador de longo prazo ou de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="98025-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="98025-118">Identificadores de curto prazo são mais fáceis e rápidos de construir, mas são limitados em seu escopo e duração, normalmente para a sessão atual e estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="98025-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="98025-119">Elas são comumente usadas para objetos de natureza temporária, como linhas de tabela ou entradas de caixa de diálogo, e então abandonadas.</span><span class="sxs-lookup"><span data-stu-id="98025-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="98025-120">Identificadores de longo prazo são usados para objetos de uma natureza mais ampla e longa.</span><span class="sxs-lookup"><span data-stu-id="98025-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="98025-121">Essa propriedade está sempre disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) após a primeira chamada para o método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="98025-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="98025-122">Alguns provedores de serviços podem torná-lo disponível imediatamente após a instaciação.</span><span class="sxs-lookup"><span data-stu-id="98025-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="98025-123">O provedor deve sempre retornar um identificador de entrada de longo prazo de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="98025-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="98025-124">Portanto, para converter um identificador de curto prazo em longo prazo, basta abrir o objeto e obter sua propriedade por meio **de GetProps**.</span><span class="sxs-lookup"><span data-stu-id="98025-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="98025-125">A tabela a seguir resume diferenças importantes entre essa propriedade, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="98025-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="98025-126">**Característica**</span><span class="sxs-lookup"><span data-stu-id="98025-126">**Characteristic**</span></span>|<span data-ttu-id="98025-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="98025-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="98025-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="98025-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="98025-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="98025-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="98025-130">Obrigatório em objetos anexos</span><span class="sxs-lookup"><span data-stu-id="98025-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="98025-131">Não</span><span class="sxs-lookup"><span data-stu-id="98025-131">No</span></span>  <br/> |<span data-ttu-id="98025-132">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-132">Yes</span></span>  <br/> |<span data-ttu-id="98025-133">Não</span><span class="sxs-lookup"><span data-stu-id="98025-133">No</span></span>  <br/> |
|<span data-ttu-id="98025-134">Obrigatório em objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="98025-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="98025-135">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-135">Yes</span></span>  <br/> |<span data-ttu-id="98025-136">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-136">Yes</span></span>  <br/> |<span data-ttu-id="98025-137">Não</span><span class="sxs-lookup"><span data-stu-id="98025-137">No</span></span>  <br/> |
|<span data-ttu-id="98025-138">Obrigatório nos objetos do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="98025-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="98025-139">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-139">Yes</span></span>  <br/> |<span data-ttu-id="98025-140">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-140">Yes</span></span>  <br/> |<span data-ttu-id="98025-141">Não</span><span class="sxs-lookup"><span data-stu-id="98025-141">No</span></span>  <br/> |
|<span data-ttu-id="98025-142">Obrigatório em objetos de status</span><span class="sxs-lookup"><span data-stu-id="98025-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="98025-143">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-143">Yes</span></span>  <br/> |<span data-ttu-id="98025-144">Não</span><span class="sxs-lookup"><span data-stu-id="98025-144">No</span></span>  <br/> |<span data-ttu-id="98025-145">Não</span><span class="sxs-lookup"><span data-stu-id="98025-145">No</span></span>  <br/> |
|<span data-ttu-id="98025-146">Criado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="98025-146">Created by client</span></span>  <br/> |<span data-ttu-id="98025-147">Não</span><span class="sxs-lookup"><span data-stu-id="98025-147">No</span></span>  <br/> |<span data-ttu-id="98025-148">Não</span><span class="sxs-lookup"><span data-stu-id="98025-148">No</span></span>  <br/> |<span data-ttu-id="98025-149">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-149">Yes</span></span>  <br/> |
|<span data-ttu-id="98025-150">Disponível antes da chamada para **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="98025-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="98025-151">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="98025-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="98025-152">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="98025-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="98025-153">Para mensagens, Sim.</span><span class="sxs-lookup"><span data-stu-id="98025-153">For messages, Yes.</span></span> <span data-ttu-id="98025-154">Para outros, depende da implementação do provedor.</span><span class="sxs-lookup"><span data-stu-id="98025-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="98025-155">Alterado em uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="98025-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="98025-156">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-156">Yes</span></span>  <br/> |<span data-ttu-id="98025-157">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-157">Yes</span></span>  <br/> |<span data-ttu-id="98025-158">Não</span><span class="sxs-lookup"><span data-stu-id="98025-158">No</span></span>  <br/> |
|<span data-ttu-id="98025-159">Alterável pelo cliente após uma cópia</span><span class="sxs-lookup"><span data-stu-id="98025-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="98025-160">Não</span><span class="sxs-lookup"><span data-stu-id="98025-160">No</span></span>  <br/> |<span data-ttu-id="98025-161">Não</span><span class="sxs-lookup"><span data-stu-id="98025-161">No</span></span>  <br/> |<span data-ttu-id="98025-162">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-162">Yes</span></span>  <br/> |
|<span data-ttu-id="98025-163">Exclusivo dentro</span><span class="sxs-lookup"><span data-stu-id="98025-163">Unique within</span></span>  <br/> |<span data-ttu-id="98025-164">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="98025-164">Entire world</span></span>  <br/> |<span data-ttu-id="98025-165">Instância do provedor</span><span class="sxs-lookup"><span data-stu-id="98025-165">Provider instance</span></span>  <br/> |<span data-ttu-id="98025-166">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="98025-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="98025-167">Binário comparável (como com memcmp)</span><span class="sxs-lookup"><span data-stu-id="98025-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="98025-168">Não use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="98025-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="98025-169">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-169">Yes</span></span>  <br/> |<span data-ttu-id="98025-170">Sim</span><span class="sxs-lookup"><span data-stu-id="98025-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="98025-171">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="98025-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98025-172">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="98025-172">Protocol specifications</span></span>

<span data-ttu-id="98025-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98025-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98025-174">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="98025-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98025-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98025-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98025-176">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="98025-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="98025-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98025-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98025-178">Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="98025-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="98025-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98025-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98025-180">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="98025-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="98025-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98025-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98025-182">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="98025-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="98025-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98025-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98025-184">Lida com a recuperação de listas de permissões de pasta armazenadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="98025-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="98025-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98025-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98025-186">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com objetos de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="98025-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="98025-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98025-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98025-188">Especifica o esquema e os métodos usados para solicitar informações de disponibilidade para usuários e recursos.</span><span class="sxs-lookup"><span data-stu-id="98025-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98025-189">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="98025-189">Header files</span></span>

<span data-ttu-id="98025-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98025-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="98025-191">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="98025-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="98025-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98025-192">Mapitags.h</span></span>
  
> <span data-ttu-id="98025-193">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="98025-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98025-194">Confira também</span><span class="sxs-lookup"><span data-stu-id="98025-194">See also</span></span>



[<span data-ttu-id="98025-195">Propriedade canônica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="98025-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="98025-196">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="98025-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98025-197">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="98025-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98025-198">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="98025-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98025-199">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="98025-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

