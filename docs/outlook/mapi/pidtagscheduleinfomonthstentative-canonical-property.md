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
ms.openlocfilehash: 20620a5835e627eb7543a03037f9be75db6739ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769969"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="29691-103">Propriedade canônica PidTagScheduleInfoMonthsTentative</span><span class="sxs-lookup"><span data-stu-id="29691-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="29691-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29691-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29691-105">Contém os meses marcados provisórios na mensagem de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="29691-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29691-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="29691-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29691-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="29691-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="29691-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="29691-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29691-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="29691-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="29691-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="29691-110">Data type:</span></span>  <br/> |<span data-ttu-id="29691-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="29691-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="29691-112">Área:</span><span class="sxs-lookup"><span data-stu-id="29691-112">Area:</span></span>  <br/> |<span data-ttu-id="29691-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="29691-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29691-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="29691-114">Remarks</span></span>

<span data-ttu-id="29691-115">O número de valores desta propriedade deve estar entre zero e o número de meses coberto pelo intervalo de publicação, que é o período entre o **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) e **PR_FREEBUSY_PUBLISH_END **Propriedades ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="29691-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="29691-116">Cada valor nessa propriedade, tem um mês e ano codificado nela.</span><span class="sxs-lookup"><span data-stu-id="29691-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="29691-117">Isso é calculado usando a expressão "ano × 16 + mês", onde o mês e ano são baseados no calendário gregoriano.</span><span class="sxs-lookup"><span data-stu-id="29691-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="29691-118">Os valores são classificados em ordem crescente e são codificados no formato pouco-endian.</span><span class="sxs-lookup"><span data-stu-id="29691-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="29691-119">Se um evento é espalhado por vários meses ou anos de vários, deve haver um valor para cada um dos meses contidos no intervalo de publicação.</span><span class="sxs-lookup"><span data-stu-id="29691-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="29691-120">Se não houver nenhum evento provisório do intervalo de publicação, esta propriedade e **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) não devem ser definido ou devem ser excluídos se eles já existirem.</span><span class="sxs-lookup"><span data-stu-id="29691-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="29691-121">Caso contrário, essa propriedade deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="29691-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="29691-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="29691-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29691-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="29691-123">Protocol specifications</span></span>

<span data-ttu-id="29691-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29691-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29691-125">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="29691-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="29691-126">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29691-126">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29691-127">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="29691-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29691-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="29691-128">Header files</span></span>

<span data-ttu-id="29691-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29691-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="29691-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="29691-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="29691-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="29691-131">Mapitags.h</span></span>
  
> <span data-ttu-id="29691-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="29691-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29691-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="29691-133">See also</span></span>



[<span data-ttu-id="29691-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="29691-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29691-135">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="29691-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29691-136">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="29691-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29691-137">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="29691-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

