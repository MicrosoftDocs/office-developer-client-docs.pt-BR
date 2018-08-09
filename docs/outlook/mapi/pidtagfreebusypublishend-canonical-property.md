---
title: Propriedade canônica PidTagFreeBusyPublishEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1f7f439b211b60f7acad3a9dd19c50a21923c1cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769278"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="7c88a-103">Propriedade canônica PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="7c88a-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="7c88a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c88a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c88a-105">Contém a hora de término do intervalo de publicação.</span><span class="sxs-lookup"><span data-stu-id="7c88a-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c88a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7c88a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c88a-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="7c88a-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="7c88a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7c88a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c88a-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="7c88a-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="7c88a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7c88a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c88a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7c88a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7c88a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7c88a-112">Area:</span></span>  <br/> |<span data-ttu-id="7c88a-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="7c88a-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c88a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c88a-114">Remarks</span></span>

<span data-ttu-id="7c88a-115">O valor dessa propriedade é computado adicionando o valor de **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) para a data de início do intervalo de publicação.</span><span class="sxs-lookup"><span data-stu-id="7c88a-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="7c88a-116">Esse valor é expresso como o número de minutos desde a meia-noite, 1 de janeiro de 1601 no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="7c88a-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7c88a-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c88a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c88a-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7c88a-118">Protocol specifications</span></span>

<span data-ttu-id="7c88a-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c88a-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c88a-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7c88a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c88a-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c88a-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c88a-122">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="7c88a-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c88a-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7c88a-123">Header files</span></span>

<span data-ttu-id="7c88a-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c88a-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c88a-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7c88a-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c88a-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c88a-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7c88a-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7c88a-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c88a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c88a-128">See also</span></span>



[<span data-ttu-id="7c88a-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7c88a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c88a-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7c88a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c88a-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7c88a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c88a-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7c88a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
