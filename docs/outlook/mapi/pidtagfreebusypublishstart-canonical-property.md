---
title: Propriedade canônica PidTagFreeBusyPublishStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishStart
api_type:
- HeaderDef
ms.assetid: d059f913-3d61-4bec-8215-5b07f0fba488
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ccee84b8e548ee656366d07c81927a701e9b70f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769308"
---
# <a name="pidtagfreebusypublishstart-canonical-property"></a><span data-ttu-id="1cde9-103">Propriedade canônica PidTagFreeBusyPublishStart</span><span class="sxs-lookup"><span data-stu-id="1cde9-103">PidTagFreeBusyPublishStart Canonical Property</span></span>

  
  
<span data-ttu-id="1cde9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1cde9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1cde9-105">Contém a hora de início do intervalo de publicação.</span><span class="sxs-lookup"><span data-stu-id="1cde9-105">Contains the start time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cde9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1cde9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cde9-107">PR_FREEBUSY_PUBLISH_START</span><span class="sxs-lookup"><span data-stu-id="1cde9-107">PR_FREEBUSY_PUBLISH_START</span></span>  <br/> |
|<span data-ttu-id="1cde9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1cde9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cde9-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="1cde9-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="1cde9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1cde9-110">Data type:</span></span>  <br/> |<span data-ttu-id="1cde9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1cde9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1cde9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1cde9-112">Area:</span></span>  <br/> |<span data-ttu-id="1cde9-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="1cde9-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cde9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cde9-114">Remarks</span></span>

<span data-ttu-id="1cde9-115">O valor desta propriedade é o número de minutos desde a meia-noite, 1 de janeiro de 1601 no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="1cde9-115">The value for this property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1cde9-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1cde9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1cde9-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1cde9-117">Protocol specifications</span></span>

<span data-ttu-id="1cde9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cde9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cde9-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1cde9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1cde9-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cde9-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cde9-121">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="1cde9-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1cde9-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1cde9-122">Header files</span></span>

<span data-ttu-id="1cde9-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cde9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cde9-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1cde9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cde9-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1cde9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1cde9-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1cde9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cde9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cde9-127">See also</span></span>



[<span data-ttu-id="1cde9-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1cde9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cde9-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1cde9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cde9-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1cde9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cde9-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1cde9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

