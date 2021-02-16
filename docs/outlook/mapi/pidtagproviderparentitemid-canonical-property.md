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
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433413"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="a1111-103">Propriedade canônica PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="a1111-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="a1111-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1111-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1111-105">Especifica um identificador para o pai de uma pasta ou um item em um armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a1111-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1111-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a1111-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1111-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="a1111-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="a1111-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a1111-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1111-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="a1111-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="a1111-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a1111-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1111-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a1111-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a1111-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a1111-112">Area:</span></span>  <br/> |<span data-ttu-id="a1111-113">MAPI não transmitível</span><span class="sxs-lookup"><span data-stu-id="a1111-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1111-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1111-114">Remarks</span></span>

<span data-ttu-id="a1111-115">Os provedores de armazenamento podem especificar um valor para essa propriedade para um pai de uma pasta ou um item, mas devem manter o mesmo valor entre sessões.</span><span class="sxs-lookup"><span data-stu-id="a1111-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="a1111-116">Os provedores de armazenamento usam essa propriedade para identificar resultados de pesquisa retornados de um mecanismo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a1111-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a1111-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1111-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a1111-118">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a1111-118">Header files</span></span>

<span data-ttu-id="a1111-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1111-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1111-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a1111-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1111-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1111-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a1111-122">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a1111-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1111-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1111-123">See also</span></span>



[<span data-ttu-id="a1111-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a1111-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1111-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a1111-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1111-126">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a1111-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1111-127">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a1111-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

