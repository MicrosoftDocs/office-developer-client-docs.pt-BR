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
ms.openlocfilehash: f3d49faba9d1e9cc8609ee55f7fb3c329e9ae947
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593036"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="9594b-103">Propriedade canônica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="9594b-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="9594b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9594b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9594b-105">Contém um identificador de entrada MAPI usado para abrir e editar as propriedades de um determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="9594b-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9594b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9594b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9594b-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9594b-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="9594b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9594b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9594b-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="9594b-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="9594b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9594b-110">Data type:</span></span>  <br/> |<span data-ttu-id="9594b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9594b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9594b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9594b-112">Area:</span></span>  <br/> |<span data-ttu-id="9594b-113">Propriedades de identificação</span><span class="sxs-lookup"><span data-stu-id="9594b-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9594b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9594b-114">Remarks</span></span>

<span data-ttu-id="9594b-115">Essa propriedade identifica um objeto para **OpenEntry** instanciar e fornece acesso a todas as suas propriedades por meio da interface derivada apropriada de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="9594b-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="9594b-116">Essa propriedade é uma das propriedades endereço base para todos os usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9594b-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="9594b-117">Essa propriedade pode conter um longo prazo ou um identificador de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="9594b-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="9594b-118">Identificadores de curto prazo são mais fácil e rápido para construção, mas estão limitados em seu escopo e a duração, geralmente para a sessão atual e a estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9594b-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="9594b-119">Elas são usadas para objetos de natureza temporária, como linhas da tabela ou entradas da caixa de diálogo e então abandonadas.</span><span class="sxs-lookup"><span data-stu-id="9594b-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="9594b-120">Identificadores de longo prazo são usados para objetos de natureza mais ampla e de longa duração.</span><span class="sxs-lookup"><span data-stu-id="9594b-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="9594b-121">Essa propriedade sempre está disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) após a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="9594b-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="9594b-122">Alguns provedores de serviços podem disponibilizá-lo imediatamente após instanciação.</span><span class="sxs-lookup"><span data-stu-id="9594b-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="9594b-123">O provedor sempre deve retornar um identificador de entrada de longo prazo do **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="9594b-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="9594b-124">Portanto, para converter um identificador curto prazo longo prazo, simplesmente abre o objeto e obter seu essa propriedade por meio de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="9594b-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="9594b-125">A tabela a seguir resume as diferenças importantes entre essa propriedade, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9594b-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="9594b-126">**Característica**</span><span class="sxs-lookup"><span data-stu-id="9594b-126">**Characteristic**</span></span>|<span data-ttu-id="9594b-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="9594b-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="9594b-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="9594b-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="9594b-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="9594b-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9594b-130">Necessários nos objetos attachment</span><span class="sxs-lookup"><span data-stu-id="9594b-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="9594b-131">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-131">No</span></span>  <br/> |<span data-ttu-id="9594b-132">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-132">Yes</span></span>  <br/> |<span data-ttu-id="9594b-133">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-133">No</span></span>  <br/> |
|<span data-ttu-id="9594b-134">Necessários nos objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="9594b-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="9594b-135">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-135">Yes</span></span>  <br/> |<span data-ttu-id="9594b-136">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-136">Yes</span></span>  <br/> |<span data-ttu-id="9594b-137">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-137">No</span></span>  <br/> |
|<span data-ttu-id="9594b-138">Necessários nos objetos de repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="9594b-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="9594b-139">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-139">Yes</span></span>  <br/> |<span data-ttu-id="9594b-140">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-140">Yes</span></span>  <br/> |<span data-ttu-id="9594b-141">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-141">No</span></span>  <br/> |
|<span data-ttu-id="9594b-142">Necessários nos objetos de status</span><span class="sxs-lookup"><span data-stu-id="9594b-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="9594b-143">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-143">Yes</span></span>  <br/> |<span data-ttu-id="9594b-144">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-144">No</span></span>  <br/> |<span data-ttu-id="9594b-145">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-145">No</span></span>  <br/> |
|<span data-ttu-id="9594b-146">Criado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="9594b-146">Created by client</span></span>  <br/> |<span data-ttu-id="9594b-147">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-147">No</span></span>  <br/> |<span data-ttu-id="9594b-148">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-148">No</span></span>  <br/> |<span data-ttu-id="9594b-149">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-149">Yes</span></span>  <br/> |
|<span data-ttu-id="9594b-150">Disponíveis antes da chamada para **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="9594b-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="9594b-151">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="9594b-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="9594b-152">Depende da implementação do provedor</span><span class="sxs-lookup"><span data-stu-id="9594b-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="9594b-153">Para mensagens, Sim.</span><span class="sxs-lookup"><span data-stu-id="9594b-153">For messages, Yes.</span></span> <span data-ttu-id="9594b-154">Para outras pessoas, depende da implementação do provedor.</span><span class="sxs-lookup"><span data-stu-id="9594b-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="9594b-155">Alterado em uma operação de cópia</span><span class="sxs-lookup"><span data-stu-id="9594b-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="9594b-156">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-156">Yes</span></span>  <br/> |<span data-ttu-id="9594b-157">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-157">Yes</span></span>  <br/> |<span data-ttu-id="9594b-158">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-158">No</span></span>  <br/> |
|<span data-ttu-id="9594b-159">Podem ser alterados pelo cliente após uma cópia</span><span class="sxs-lookup"><span data-stu-id="9594b-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="9594b-160">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-160">No</span></span>  <br/> |<span data-ttu-id="9594b-161">Não</span><span class="sxs-lookup"><span data-stu-id="9594b-161">No</span></span>  <br/> |<span data-ttu-id="9594b-162">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-162">Yes</span></span>  <br/> |
|<span data-ttu-id="9594b-163">Exclusiva dentro</span><span class="sxs-lookup"><span data-stu-id="9594b-163">Unique within</span></span>  <br/> |<span data-ttu-id="9594b-164">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="9594b-164">Entire world</span></span>  <br/> |<span data-ttu-id="9594b-165">Instância do provedor</span><span class="sxs-lookup"><span data-stu-id="9594b-165">Provider instance</span></span>  <br/> |<span data-ttu-id="9594b-166">Mundo inteiro</span><span class="sxs-lookup"><span data-stu-id="9594b-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="9594b-167">Binário comparável (assim como acontece com memcmp)</span><span class="sxs-lookup"><span data-stu-id="9594b-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="9594b-168">Sem uso [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="9594b-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="9594b-169">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-169">Yes</span></span>  <br/> |<span data-ttu-id="9594b-170">Sim</span><span class="sxs-lookup"><span data-stu-id="9594b-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9594b-171">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9594b-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9594b-172">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9594b-172">Protocol specifications</span></span>

<span data-ttu-id="9594b-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9594b-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9594b-174">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9594b-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9594b-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9594b-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9594b-176">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="9594b-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9594b-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9594b-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9594b-178">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="9594b-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="9594b-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9594b-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9594b-180">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9594b-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="9594b-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9594b-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9594b-182">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="9594b-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="9594b-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9594b-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9594b-184">Trata a recuperação de listas de permissão de pastas que são armazenados no servidor.</span><span class="sxs-lookup"><span data-stu-id="9594b-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="9594b-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9594b-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9594b-186">Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="9594b-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="9594b-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9594b-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9594b-188">Especifica o esquema e métodos que são usados para solicitar informações de disponibilidade para usuários e recursos.</span><span class="sxs-lookup"><span data-stu-id="9594b-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9594b-189">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9594b-189">Header files</span></span>

<span data-ttu-id="9594b-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9594b-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="9594b-191">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9594b-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="9594b-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9594b-192">Mapitags.h</span></span>
  
> <span data-ttu-id="9594b-193">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="9594b-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9594b-194">Confira também</span><span class="sxs-lookup"><span data-stu-id="9594b-194">See also</span></span>



[<span data-ttu-id="9594b-195">Propriedade canônica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="9594b-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="9594b-196">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9594b-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9594b-197">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="9594b-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9594b-198">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9594b-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9594b-199">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9594b-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

