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
ms.openlocfilehash: 691c5977092b5e2ca6b453209982dd1333a6df89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769097"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="f5938-103">Propriedade canônica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="f5938-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="f5938-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5938-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5938-105">Contém um objeto table de hierarquia incorporado que fornece informações sobre o filho contêineres.</span><span class="sxs-lookup"><span data-stu-id="f5938-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5938-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f5938-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5938-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="f5938-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="f5938-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f5938-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5938-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="f5938-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="f5938-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f5938-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5938-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="f5938-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="f5938-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f5938-112">Area:</span></span>  <br/> |<span data-ttu-id="f5938-113">Container</span><span class="sxs-lookup"><span data-stu-id="f5938-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5938-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5938-114">Remarks</span></span>

<span data-ttu-id="f5938-115">Essa propriedade pode ser excluída em operações [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações da [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="f5938-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="f5938-116">Como uma propriedade do tipo **PT_OBJECT**, ele não pode ser recuperado com êxito pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) ; seu conteúdo deve ser acessado pelo método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="f5938-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="f5938-117">Provedores de serviços devem relatá-la para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas pode, opcionalmente, relatá-la ou não se não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="f5938-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="f5938-118">Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) .</span><span class="sxs-lookup"><span data-stu-id="f5938-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="f5938-119">Para obter mais informações, consulte as [Tabelas de hierarquias](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f5938-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="f5938-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), essa propriedade e **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) são semelhantes em uso.</span><span class="sxs-lookup"><span data-stu-id="f5938-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="f5938-121">Várias propriedades MAPI fornecem acesso às tabelas:</span><span class="sxs-lookup"><span data-stu-id="f5938-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="f5938-122">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="f5938-122">**Property**</span></span>|<span data-ttu-id="f5938-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="f5938-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5938-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f5938-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f5938-125">Tabela de conteúdo</span><span class="sxs-lookup"><span data-stu-id="f5938-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="f5938-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="f5938-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="f5938-127">Tabela de hierarquia</span><span class="sxs-lookup"><span data-stu-id="f5938-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="f5938-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f5938-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f5938-129">Tabela de conteúdo associado</span><span class="sxs-lookup"><span data-stu-id="f5938-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="f5938-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f5938-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f5938-131">Tabela de anexos</span><span class="sxs-lookup"><span data-stu-id="f5938-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="f5938-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f5938-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f5938-133">Tabela de destinatários</span><span class="sxs-lookup"><span data-stu-id="f5938-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f5938-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5938-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5938-135">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f5938-135">Protocol specifications</span></span>

<span data-ttu-id="f5938-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5938-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5938-137">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f5938-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5938-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5938-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5938-139">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="f5938-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f5938-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5938-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5938-141">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="f5938-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5938-142">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f5938-142">Header files</span></span>

<span data-ttu-id="f5938-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5938-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5938-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f5938-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5938-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5938-145">Mapitags.h</span></span>
  
> <span data-ttu-id="f5938-146">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f5938-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5938-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5938-147">See also</span></span>



[<span data-ttu-id="f5938-148">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f5938-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5938-149">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f5938-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5938-150">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f5938-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5938-151">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f5938-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

