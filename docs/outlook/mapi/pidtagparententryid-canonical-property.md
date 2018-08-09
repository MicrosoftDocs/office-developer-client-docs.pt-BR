---
title: Propriedade canônica PidTagParentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentEntryId
api_type:
- COM
ms.assetid: 55e08ace-493c-4246-8ebf-c304f4abc56a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ba30514df028805135e9e31e7214ca336b1b3f85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769656"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="2ea5a-103">Propriedade canônica PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="2ea5a-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="2ea5a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ea5a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ea5a-105">Contém o identificador de entrada da pasta que contém uma pasta ou mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ea5a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2ea5a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ea5a-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2ea5a-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="2ea5a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2ea5a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ea5a-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="2ea5a-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="2ea5a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2ea5a-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ea5a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2ea5a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2ea5a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2ea5a-112">Area:</span></span>  <br/> |<span data-ttu-id="2ea5a-113">Propriedades de identificação</span><span class="sxs-lookup"><span data-stu-id="2ea5a-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ea5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ea5a-114">Remarks</span></span>

<span data-ttu-id="2ea5a-115">Essa propriedade é computada pelo repositórios de mensagem para todas as mensagens e pastas.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="2ea5a-116">Para uma pasta de raiz do repositório de mensagem, essa propriedade contém o identificador de entrada da pasta.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="2ea5a-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) e essa propriedade não estão relacionados entre si.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="2ea5a-118">Eles pertencem ao contextos completamente diferentes.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ea5a-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ea5a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ea5a-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2ea5a-120">Protocol specifications</span></span>

<span data-ttu-id="2ea5a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ea5a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ea5a-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ea5a-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ea5a-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ea5a-124">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="2ea5a-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ea5a-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ea5a-126">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-126">Handles folder operations.</span></span>
    
<span data-ttu-id="2ea5a-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ea5a-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ea5a-128">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="2ea5a-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ea5a-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ea5a-130">Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="2ea5a-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ea5a-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ea5a-132">Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="2ea5a-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ea5a-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ea5a-134">Especifica o método de fornecimento de dados do OAB (catálogo) de endereços offline do servidor para o cliente.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ea5a-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2ea5a-135">Header files</span></span>

<span data-ttu-id="2ea5a-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ea5a-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ea5a-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ea5a-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ea5a-138">Mapitags.h</span></span>
  
> <span data-ttu-id="2ea5a-139">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2ea5a-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ea5a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ea5a-140">See also</span></span>



[<span data-ttu-id="2ea5a-141">Propriedade canônica PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="2ea5a-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="2ea5a-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2ea5a-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ea5a-143">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2ea5a-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ea5a-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2ea5a-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ea5a-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2ea5a-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

