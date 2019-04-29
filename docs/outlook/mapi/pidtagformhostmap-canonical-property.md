---
title: Propriedade canônica PidTagFormHostMap
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 346776635fc36ffd8efd10cb232846831add20f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433763"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="b7fc9-103">Propriedade canônica PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="b7fc9-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="b7fc9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7fc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7fc9-105">Contém um mapa de Hospedagem de formulários disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7fc9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b7fc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7fc9-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="b7fc9-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="b7fc9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b7fc9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7fc9-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="b7fc9-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="b7fc9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b7fc9-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7fc9-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="b7fc9-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="b7fc9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b7fc9-112">Area:</span></span>  <br/> |<span data-ttu-id="b7fc9-113">MAPI comum</span><span class="sxs-lookup"><span data-stu-id="b7fc9-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7fc9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7fc9-114">Remarks</span></span>

<span data-ttu-id="b7fc9-115">Um aplicativo cliente deve atualizar essa propriedade, juntamente com a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), ao alterar a estrutura subjacente na interface do **IMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="b7fc9-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b7fc9-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7fc9-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b7fc9-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b7fc9-117">Header files</span></span>

<span data-ttu-id="b7fc9-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b7fc9-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7fc9-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7fc9-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b7fc9-120">Mapitags.h</span></span>
  
> <span data-ttu-id="b7fc9-121">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7fc9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7fc9-122">See also</span></span>



[<span data-ttu-id="b7fc9-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b7fc9-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7fc9-124">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b7fc9-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7fc9-125">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b7fc9-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7fc9-126">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b7fc9-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

