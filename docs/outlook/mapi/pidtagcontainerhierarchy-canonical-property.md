---
title: Propriedade canônica PidTagContainerHierarchy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332855"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="8f03e-103">Propriedade canônica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="8f03e-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="8f03e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f03e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f03e-105">Contém um objeto de tabela de hierarquia incorporado que fornece informações sobre os contêineres filhos.</span><span class="sxs-lookup"><span data-stu-id="8f03e-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f03e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8f03e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f03e-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="8f03e-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="8f03e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8f03e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f03e-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="8f03e-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="8f03e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8f03e-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f03e-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="8f03e-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="8f03e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8f03e-112">Area:</span></span>  <br/> |<span data-ttu-id="8f03e-113">Contêiner</span><span class="sxs-lookup"><span data-stu-id="8f03e-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f03e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f03e-114">Remarks</span></span>

<span data-ttu-id="8f03e-115">Esta propriedade pode ser excluída nas operações de [IMAPIProp:: CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="8f03e-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="8f03e-116">Como uma propriedade do tipo **PT_OBJECT**, ela não pode ser recuperada com êxito pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps; seu conteúdo deve ser acessado pelo método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="8f03e-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="8f03e-117">Os provedores de serviços devem relatá-lo para o método [IMAPIProp::](imapiprop-getproplist.md) getproplist, se estiver definido, mas pode opcionalmente relatá-lo ou não se ele não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="8f03e-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="8f03e-118">Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMAPIContainer::](imapicontainer-gethierarchytable.md) GetHierarchyTable.</span><span class="sxs-lookup"><span data-stu-id="8f03e-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="8f03e-119">Para obter mais informações, consulte [tabelas de hierarquia](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8f03e-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="8f03e-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), e essa propriedade é semelhante ao uso.</span><span class="sxs-lookup"><span data-stu-id="8f03e-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="8f03e-121">Várias propriedades MAPI fornecem acesso a tabelas:</span><span class="sxs-lookup"><span data-stu-id="8f03e-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="8f03e-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="8f03e-122">**Property**</span></span>|<span data-ttu-id="8f03e-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="8f03e-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8f03e-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8f03e-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8f03e-125">Tabela de conteúdo</span><span class="sxs-lookup"><span data-stu-id="8f03e-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="8f03e-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="8f03e-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="8f03e-127">Tabela de hierarquia</span><span class="sxs-lookup"><span data-stu-id="8f03e-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="8f03e-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8f03e-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8f03e-129">Tabela de conteúdo associado</span><span class="sxs-lookup"><span data-stu-id="8f03e-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="8f03e-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8f03e-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8f03e-131">Tabela de anexos</span><span class="sxs-lookup"><span data-stu-id="8f03e-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="8f03e-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8f03e-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8f03e-133">Tabela de destinatários</span><span class="sxs-lookup"><span data-stu-id="8f03e-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8f03e-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f03e-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f03e-135">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="8f03e-135">Protocol specifications</span></span>

<span data-ttu-id="8f03e-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f03e-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f03e-137">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8f03e-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8f03e-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f03e-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f03e-139">Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="8f03e-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8f03e-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f03e-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f03e-141">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="8f03e-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f03e-142">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8f03e-142">Header files</span></span>

<span data-ttu-id="8f03e-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8f03e-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f03e-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8f03e-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f03e-145">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8f03e-145">Mapitags.h</span></span>
  
> <span data-ttu-id="8f03e-146">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8f03e-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f03e-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f03e-147">See also</span></span>



[<span data-ttu-id="8f03e-148">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8f03e-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f03e-149">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8f03e-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f03e-150">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8f03e-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f03e-151">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8f03e-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

