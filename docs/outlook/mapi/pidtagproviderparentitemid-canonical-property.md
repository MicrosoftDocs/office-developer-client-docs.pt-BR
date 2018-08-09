---
title: Propriedade canônica PidTagProviderParentItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96a9d153fadbe8b4c8baa8532b8c99771b1d7987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769702"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="cc9c4-103">Propriedade canônica PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="cc9c4-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="cc9c4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc9c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc9c4-105">Especifica um identificador para o pai de uma pasta ou um item em um repositório.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc9c4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cc9c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc9c4-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="cc9c4-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="cc9c4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cc9c4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc9c4-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="cc9c4-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="cc9c4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cc9c4-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc9c4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cc9c4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cc9c4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cc9c4-112">Area:</span></span>  <br/> |<span data-ttu-id="cc9c4-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="cc9c4-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc9c4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc9c4-114">Remarks</span></span>

<span data-ttu-id="cc9c4-115">Provedores de armazenamento podem especificar um valor para essa propriedade para um pai de uma pasta ou um item, mas devem manter o valor os mesmos entre sessões.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="cc9c4-116">Provedores de armazenamento usam essa propriedade para identificar os resultados de pesquisa retornados de um mecanismo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cc9c4-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc9c4-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cc9c4-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cc9c4-118">Header files</span></span>

<span data-ttu-id="cc9c4-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc9c4-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc9c4-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc9c4-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc9c4-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cc9c4-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc9c4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc9c4-123">See also</span></span>



[<span data-ttu-id="cc9c4-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cc9c4-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc9c4-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cc9c4-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc9c4-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cc9c4-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc9c4-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cc9c4-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

