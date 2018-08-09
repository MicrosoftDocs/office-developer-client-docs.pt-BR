---
title: Propriedade canônica PidTagContainerContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c2979a0825ad6c62dbbb7931255501e90d8450a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769085"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="b0d0f-103">Propriedade canônica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="b0d0f-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="b0d0f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0d0f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0d0f-105">Contém um objeto table de conteúdo incorporado que fornece informações sobre um contêiner.</span><span class="sxs-lookup"><span data-stu-id="b0d0f-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0d0f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b0d0f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0d0f-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="b0d0f-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="b0d0f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b0d0f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0d0f-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="b0d0f-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="b0d0f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b0d0f-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0d0f-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b0d0f-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="b0d0f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b0d0f-112">Area:</span></span>  <br/> |<span data-ttu-id="b0d0f-113">Container</span><span class="sxs-lookup"><span data-stu-id="b0d0f-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0d0f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0d0f-114">Remarks</span></span>

<span data-ttu-id="b0d0f-115">Essa propriedade pode ser excluída em operações [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações da [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="b0d0f-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="b0d0f-116">Como uma propriedade do tipo PT_OBJECT, ele não pode ser recuperado com êxito pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) ; seu conteúdo deve ser acessado pelo método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="b0d0f-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="b0d0f-117">Provedores de serviços devem relatá-la para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas pode, opcionalmente, relatá-la ou não se não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="b0d0f-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="b0d0f-118">Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="b0d0f-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="b0d0f-119">Para obter mais informações, consulte [As tabelas de conteúdo](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b0d0f-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="b0d0f-120">Essa propriedade, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) e **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) são semelhantes em uso.</span><span class="sxs-lookup"><span data-stu-id="b0d0f-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="b0d0f-121">Várias propriedades MAPI fornecem acesso às tabelas:</span><span class="sxs-lookup"><span data-stu-id="b0d0f-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="b0d0f-122">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="b0d0f-122">**Property**</span></span>|<span data-ttu-id="b0d0f-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="b0d0f-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0d0f-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="b0d0f-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="b0d0f-125">Tabela de conteúdo</span><span class="sxs-lookup"><span data-stu-id="b0d0f-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="b0d0f-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0d0f-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0d0f-127">Tabela de hierarquia</span><span class="sxs-lookup"><span data-stu-id="b0d0f-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="b0d0f-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0d0f-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0d0f-129">Tabela de conteúdo associado</span><span class="sxs-lookup"><span data-stu-id="b0d0f-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="b0d0f-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0d0f-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0d0f-131">Tabela de anexos</span><span class="sxs-lookup"><span data-stu-id="b0d0f-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="b0d0f-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0d0f-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0d0f-133">Tabela de destinatários</span><span class="sxs-lookup"><span data-stu-id="b0d0f-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b0d0f-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0d0f-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0d0f-135">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b0d0f-135">Protocol specifications</span></span>

<span data-ttu-id="b0d0f-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0d0f-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0d0f-137">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b0d0f-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0d0f-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0d0f-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0d0f-139">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="b0d0f-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0d0f-140">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b0d0f-140">Header files</span></span>

<span data-ttu-id="b0d0f-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0d0f-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0d0f-142">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b0d0f-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0d0f-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0d0f-143">Mapitags.h</span></span>
  
> <span data-ttu-id="b0d0f-144">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b0d0f-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0d0f-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0d0f-145">See also</span></span>



[<span data-ttu-id="b0d0f-146">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d0f-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0d0f-147">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b0d0f-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0d0f-148">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d0f-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0d0f-149">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b0d0f-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
