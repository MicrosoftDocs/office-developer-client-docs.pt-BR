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
ms.openlocfilehash: e0f13b0b8d2f7eb6fd7ba60e9e351b62251aa13d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572834"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="669ed-103">Propriedade canônica PidTagProviderItemId</span><span class="sxs-lookup"><span data-stu-id="669ed-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="669ed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="669ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="669ed-105">Especifica um identificador para uma pasta ou um item em um repositório.</span><span class="sxs-lookup"><span data-stu-id="669ed-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="669ed-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="669ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="669ed-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="669ed-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="669ed-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="669ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="669ed-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="669ed-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="669ed-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="669ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="669ed-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="669ed-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="669ed-112">Área:</span><span class="sxs-lookup"><span data-stu-id="669ed-112">Area:</span></span>  <br/> |<span data-ttu-id="669ed-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="669ed-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="669ed-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="669ed-114">Remarks</span></span>

<span data-ttu-id="669ed-115">Provedores de armazenamento podem especificar um valor para essa propriedade para uma pasta ou um item, mas devem manter o valor os mesmos entre sessões.</span><span class="sxs-lookup"><span data-stu-id="669ed-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="669ed-116">Provedores de armazenamento usam essa propriedade para identificar os resultados de pesquisa retornados de um mecanismo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="669ed-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="669ed-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="669ed-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="669ed-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="669ed-118">Header files</span></span>

<span data-ttu-id="669ed-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="669ed-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="669ed-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="669ed-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="669ed-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="669ed-121">Mapitags.h</span></span>
  
> <span data-ttu-id="669ed-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="669ed-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="669ed-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="669ed-123">See also</span></span>



[<span data-ttu-id="669ed-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="669ed-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="669ed-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="669ed-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="669ed-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="669ed-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="669ed-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="669ed-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

