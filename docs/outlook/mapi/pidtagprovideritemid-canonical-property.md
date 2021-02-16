---
title: Propriedade canônica PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 48653b86d625da963b655dbd1acc01a46f4687dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412118"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="e5e28-103">Propriedade canônica PidTagProviderItemId</span><span class="sxs-lookup"><span data-stu-id="e5e28-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="e5e28-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5e28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5e28-105">Especifica um identificador para uma pasta ou um item em um armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5e28-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5e28-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e5e28-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5e28-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="e5e28-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="e5e28-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e5e28-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5e28-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="e5e28-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="e5e28-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e5e28-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5e28-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e5e28-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e5e28-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e5e28-112">Area:</span></span>  <br/> |<span data-ttu-id="e5e28-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="e5e28-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5e28-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5e28-114">Remarks</span></span>

<span data-ttu-id="e5e28-115">Os provedores de armazenamento podem especificar um valor para essa propriedade para uma pasta ou um item, mas devem manter o mesmo valor entre sessões.</span><span class="sxs-lookup"><span data-stu-id="e5e28-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="e5e28-116">Os provedores de armazenamento usam essa propriedade para identificar resultados de pesquisa retornados de um mecanismo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e5e28-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e5e28-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5e28-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e5e28-118">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="e5e28-118">Header files</span></span>

<span data-ttu-id="e5e28-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5e28-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5e28-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e5e28-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5e28-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e5e28-121">Mapitags.h</span></span>
  
> <span data-ttu-id="e5e28-122">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e5e28-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5e28-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5e28-123">See also</span></span>



[<span data-ttu-id="e5e28-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e5e28-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5e28-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e5e28-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5e28-126">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e5e28-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5e28-127">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e5e28-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

