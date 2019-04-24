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
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316300"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="7016f-103">Propriedade canônica PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="7016f-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="7016f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7016f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7016f-105">Contém um objeto da tabela de conteúdo incorporado que fornece informações sobre a tabela de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="7016f-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7016f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7016f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7016f-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="7016f-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="7016f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7016f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7016f-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="7016f-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="7016f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7016f-110">Data type:</span></span>  <br/> |<span data-ttu-id="7016f-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="7016f-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="7016f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7016f-112">Area:</span></span>  <br/> |<span data-ttu-id="7016f-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="7016f-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7016f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7016f-114">Remarks</span></span>

<span data-ttu-id="7016f-115">A tabela de conteúdo associada representa uma subpasta que não aparece na tabela conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="7016f-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="7016f-116">Ele contém as mensagens associadas, ou ocultas, da pasta.</span><span class="sxs-lookup"><span data-stu-id="7016f-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="7016f-117">Esta propriedade pode ser excluída nas operações de [IMAPIProp:: CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="7016f-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="7016f-118">Como uma propriedade do tipo **PT_OBJECT**, ela não pode ser recuperada com êxito pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps; seu conteúdo deve ser acessado pelo método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="7016f-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="7016f-119">Os provedores de serviços devem relatá-lo para o método [IMAPIProp::](imapiprop-getproplist.md) getproplist, se estiver definido, mas pode opcionalmente relatá-lo ou não se ele não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="7016f-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="7016f-120">Para recuperar o conteúdo da tabela, os aplicativos cliente devem chamar o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable.</span><span class="sxs-lookup"><span data-stu-id="7016f-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="7016f-121">Para obter mais informações sobre tabelas de conteúdo da pasta, consulte [tabelas de conteúdo](contents-tables.md) e [exibição de uma tabela de conteúdo da pasta](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="7016f-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="7016f-122">O **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), e essa propriedade é semelhante ao uso.</span><span class="sxs-lookup"><span data-stu-id="7016f-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="7016f-123">Várias propriedades MAPI fornecem acesso a tabelas:</span><span class="sxs-lookup"><span data-stu-id="7016f-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="7016f-124">**Property**</span><span class="sxs-lookup"><span data-stu-id="7016f-124">**Property**</span></span>|<span data-ttu-id="7016f-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="7016f-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7016f-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7016f-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7016f-127">Tabela de conteúdo</span><span class="sxs-lookup"><span data-stu-id="7016f-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="7016f-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7016f-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7016f-129">Tabela de hierarquia</span><span class="sxs-lookup"><span data-stu-id="7016f-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="7016f-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="7016f-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="7016f-131">Tabela de conteúdo associado</span><span class="sxs-lookup"><span data-stu-id="7016f-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="7016f-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7016f-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7016f-133">Tabela de anexos</span><span class="sxs-lookup"><span data-stu-id="7016f-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="7016f-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7016f-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7016f-135">Tabela de destinatários</span><span class="sxs-lookup"><span data-stu-id="7016f-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7016f-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7016f-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7016f-137">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="7016f-137">Protocol specifications</span></span>

<span data-ttu-id="7016f-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7016f-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7016f-139">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7016f-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7016f-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7016f-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7016f-141">Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="7016f-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="7016f-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7016f-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7016f-143">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os itens de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="7016f-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7016f-144">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7016f-144">Header files</span></span>

<span data-ttu-id="7016f-145">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7016f-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="7016f-146">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7016f-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="7016f-147">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7016f-147">Mapitags.h</span></span>
  
> <span data-ttu-id="7016f-148">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7016f-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7016f-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="7016f-149">See also</span></span>



[<span data-ttu-id="7016f-150">Propriedade canônica PidTagAssociatedContentCount</span><span class="sxs-lookup"><span data-stu-id="7016f-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="7016f-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7016f-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7016f-152">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7016f-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7016f-153">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7016f-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7016f-154">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7016f-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

