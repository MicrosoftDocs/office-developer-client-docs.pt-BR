---
title: Propriedade canônica PidTagScheduleInfoMonthsTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359756"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="252ce-103">Propriedade canônica PidTagScheduleInfoMonthsTentative</span><span class="sxs-lookup"><span data-stu-id="252ce-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="252ce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="252ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="252ce-105">Contém os meses marcados como provisórios na mensagem de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="252ce-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="252ce-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="252ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="252ce-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="252ce-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="252ce-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="252ce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="252ce-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="252ce-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="252ce-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="252ce-110">Data type:</span></span>  <br/> |<span data-ttu-id="252ce-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="252ce-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="252ce-112">Área:</span><span class="sxs-lookup"><span data-stu-id="252ce-112">Area:</span></span>  <br/> |<span data-ttu-id="252ce-113">Livre/Ocupado</span><span class="sxs-lookup"><span data-stu-id="252ce-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="252ce-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="252ce-114">Remarks</span></span>

<span data-ttu-id="252ce-115">O número de valores nesta propriedade deve estar entre zero e o número de meses cobertos pelo intervalo de publicação, que é o período entre as propriedades **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) e **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="252ce-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="252ce-116">Cada valor nessa propriedade tem um mês e um ano codificados nele.</span><span class="sxs-lookup"><span data-stu-id="252ce-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="252ce-117">Isso é calculado usando a expressão "ano × 16 + mês" onde ano e mês são baseados no calendário gregoriano.</span><span class="sxs-lookup"><span data-stu-id="252ce-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="252ce-118">Os valores são organizados em ordem crescente e codificados no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="252ce-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="252ce-119">Se um evento for espalhado por vários meses ou vários anos, deverá haver um valor para cada um dos meses que se enquadram no intervalo de publicação.</span><span class="sxs-lookup"><span data-stu-id="252ce-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="252ce-120">Se não houver eventos provisórios no intervalo de publicação, essa propriedade e **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) não devem ser definidos ou devem ser excluídos se já existirem.</span><span class="sxs-lookup"><span data-stu-id="252ce-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="252ce-121">Caso contrário, essa propriedade deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="252ce-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="252ce-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="252ce-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="252ce-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="252ce-123">Protocol specifications</span></span>

<span data-ttu-id="252ce-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="252ce-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="252ce-125">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="252ce-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="252ce-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="252ce-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="252ce-127">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="252ce-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="252ce-128">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="252ce-128">Header files</span></span>

<span data-ttu-id="252ce-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="252ce-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="252ce-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="252ce-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="252ce-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="252ce-131">Mapitags.h</span></span>
  
> <span data-ttu-id="252ce-132">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="252ce-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="252ce-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="252ce-133">See also</span></span>



[<span data-ttu-id="252ce-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="252ce-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="252ce-135">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="252ce-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="252ce-136">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="252ce-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="252ce-137">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="252ce-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

