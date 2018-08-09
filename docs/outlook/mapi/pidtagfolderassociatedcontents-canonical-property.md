---
title: Propriedade canônica PidTagFolderAssociatedContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe6395029e312a19bce6252e73b4616bb0aa0851
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769242"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="f322b-103">Propriedade canônica PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="f322b-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="f322b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f322b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f322b-105">Contém um objeto table de conteúdo incorporado que fornece informações sobre a tabela de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="f322b-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f322b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f322b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f322b-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="f322b-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="f322b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f322b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f322b-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="f322b-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="f322b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f322b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f322b-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="f322b-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="f322b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f322b-112">Area:</span></span>  <br/> |<span data-ttu-id="f322b-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="f322b-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f322b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f322b-114">Remarks</span></span>

<span data-ttu-id="f322b-115">A tabela de conteúdo associado representa uma subpasta que não aparecem na tabela de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="f322b-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="f322b-116">Ele contém mensagens de associado ou ocultos, da pasta.</span><span class="sxs-lookup"><span data-stu-id="f322b-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="f322b-117">Essa propriedade pode ser excluída em operações [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações da [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="f322b-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="f322b-118">Como uma propriedade do tipo **PT_OBJECT**, ele não pode ser recuperado com êxito pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) ; seu conteúdo deve ser acessado pelo método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="f322b-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="f322b-119">Provedores de serviços devem relatá-la para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas opcionalmente relatá-la ou não se ele não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="f322b-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="f322b-120">Para recuperar o conteúdo da tabela, os aplicativos cliente devem chamar o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="f322b-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="f322b-121">Para obter mais informações sobre tabelas de conteúdo de pasta, consulte [Tabelas de conteúdo](contents-tables.md) e [exibindo uma tabela de conteúdo de pasta](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="f322b-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="f322b-122">Essa propriedade, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) e **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) são semelhantes em uso.</span><span class="sxs-lookup"><span data-stu-id="f322b-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="f322b-123">Várias propriedades MAPI fornecem acesso às tabelas:</span><span class="sxs-lookup"><span data-stu-id="f322b-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="f322b-124">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="f322b-124">**Property**</span></span>|<span data-ttu-id="f322b-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="f322b-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f322b-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f322b-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f322b-127">Tabela de conteúdo</span><span class="sxs-lookup"><span data-stu-id="f322b-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="f322b-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f322b-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f322b-129">Tabela de hierarquia</span><span class="sxs-lookup"><span data-stu-id="f322b-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="f322b-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="f322b-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="f322b-131">Tabela de conteúdo associado</span><span class="sxs-lookup"><span data-stu-id="f322b-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="f322b-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f322b-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f322b-133">Tabela de anexos</span><span class="sxs-lookup"><span data-stu-id="f322b-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="f322b-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f322b-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f322b-135">Tabela de destinatários</span><span class="sxs-lookup"><span data-stu-id="f322b-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f322b-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f322b-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f322b-137">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f322b-137">Protocol specifications</span></span>

<span data-ttu-id="f322b-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f322b-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f322b-139">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f322b-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f322b-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f322b-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f322b-141">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="f322b-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f322b-142">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f322b-142">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f322b-143">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e itens de reunião.</span><span class="sxs-lookup"><span data-stu-id="f322b-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f322b-144">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f322b-144">Header files</span></span>

<span data-ttu-id="f322b-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f322b-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="f322b-146">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f322b-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="f322b-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f322b-147">Mapitags.h</span></span>
  
> <span data-ttu-id="f322b-148">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f322b-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f322b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="f322b-149">See also</span></span>



[<span data-ttu-id="f322b-150">Propriedade canônica PidTagAssociatedContentCount</span><span class="sxs-lookup"><span data-stu-id="f322b-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="f322b-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f322b-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f322b-152">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f322b-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f322b-153">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f322b-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f322b-154">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f322b-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

