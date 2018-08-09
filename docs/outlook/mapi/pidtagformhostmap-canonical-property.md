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
ms.openlocfilehash: 9e0316ead2adf00619bd87c57946ba72ed01f4b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769285"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="dfe03-103">Propriedade canônica PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="dfe03-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="dfe03-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dfe03-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dfe03-105">Contém um mapa de host de formulários disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dfe03-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfe03-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dfe03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dfe03-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="dfe03-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="dfe03-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dfe03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dfe03-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="dfe03-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="dfe03-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dfe03-110">Data type:</span></span>  <br/> |<span data-ttu-id="dfe03-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="dfe03-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="dfe03-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dfe03-112">Area:</span></span>  <br/> |<span data-ttu-id="dfe03-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="dfe03-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfe03-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfe03-114">Remarks</span></span>

<span data-ttu-id="dfe03-115">Um aplicativo cliente deverá atualizar essa propriedade, juntamente com a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), ao alterar a estrutura subjacente na interface do **IMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="dfe03-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dfe03-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dfe03-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dfe03-117">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dfe03-117">Header files</span></span>

<span data-ttu-id="dfe03-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dfe03-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="dfe03-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dfe03-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="dfe03-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dfe03-120">Mapitags.h</span></span>
  
> <span data-ttu-id="dfe03-121">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="dfe03-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dfe03-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfe03-122">See also</span></span>



[<span data-ttu-id="dfe03-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dfe03-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dfe03-124">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="dfe03-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dfe03-125">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dfe03-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dfe03-126">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dfe03-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

