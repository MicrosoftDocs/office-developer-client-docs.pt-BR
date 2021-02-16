---
title: Propriedade canônica PidTagContentCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331952"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="ab6f2-103">Propriedade canônica PidTagContentCount</span><span class="sxs-lookup"><span data-stu-id="ab6f2-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="ab6f2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab6f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab6f2-105">Contém o número de mensagens em uma pasta, conforme calculado pelo armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab6f2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ab6f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab6f2-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="ab6f2-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="ab6f2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ab6f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab6f2-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="ab6f2-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="ab6f2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ab6f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab6f2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ab6f2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ab6f2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ab6f2-112">Area:</span></span>  <br/> |<span data-ttu-id="ab6f2-113">Folder</span><span class="sxs-lookup"><span data-stu-id="ab6f2-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab6f2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab6f2-114">Remarks</span></span>

<span data-ttu-id="ab6f2-115">Essa propriedade calculada pelo armazenamento de mensagens é usada para duas finalidades diferentes, porém relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="ab6f2-116">Em um objeto MapiFolder, ele contém o número de mensagens em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="ab6f2-117">Em uma linha de título em tabelas MAPI categorizadas, ela contém o número de mensagens não associadas na categoria correspondente a essa linha de título.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="ab6f2-118">O número contido nessa propriedade não inclui entradas associadas na pasta.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="ab6f2-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contém a contagem de mensagens não lidas para a pasta.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="ab6f2-120">Um aplicativo cliente pode ler, mas não alterar essa propriedade **e PR_CONTENT_UNREAD**.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ab6f2-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab6f2-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab6f2-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ab6f2-122">Protocol specifications</span></span>

<span data-ttu-id="ab6f2-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab6f2-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab6f2-124">Fornece referências a especificações de protocolo do Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab6f2-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab6f2-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab6f2-126">Lida com operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-126">Handles folder operations.</span></span>
    
<span data-ttu-id="ab6f2-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab6f2-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab6f2-128">Inclui operações permitidas para os objetos de tabela principais.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab6f2-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="ab6f2-129">Header files</span></span>

<span data-ttu-id="ab6f2-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab6f2-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab6f2-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab6f2-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ab6f2-132">Mapitags.h</span></span>
  
> <span data-ttu-id="ab6f2-133">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ab6f2-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab6f2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab6f2-134">See also</span></span>



[<span data-ttu-id="ab6f2-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ab6f2-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab6f2-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ab6f2-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab6f2-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ab6f2-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab6f2-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ab6f2-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

