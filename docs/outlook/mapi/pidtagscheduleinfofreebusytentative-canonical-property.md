---
title: Propriedade canônica PidTagScheduleInfoFreeBusyTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385113"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a><span data-ttu-id="217b4-103">Propriedade canônica PidTagScheduleInfoFreeBusyTentative</span><span class="sxs-lookup"><span data-stu-id="217b4-103">PidTagScheduleInfoFreeBusyTentative Canonical Property</span></span>

  
  
<span data-ttu-id="217b4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="217b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="217b4-105">Contém os blocos de vezes para o qual o status livre/ocupado é provisório.</span><span class="sxs-lookup"><span data-stu-id="217b4-105">Contains the blocks of times for which the free/busy status is tentative.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="217b4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="217b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="217b4-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="217b4-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="217b4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="217b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="217b4-109">0x6852</span><span class="sxs-lookup"><span data-stu-id="217b4-109">0x6852</span></span>  <br/> |
|<span data-ttu-id="217b4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="217b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="217b4-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="217b4-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="217b4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="217b4-112">Area:</span></span>  <br/> |<span data-ttu-id="217b4-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="217b4-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="217b4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="217b4-114">Remarks</span></span>

<span data-ttu-id="217b4-115">Esta propriedade tem quantos valores conforme o número de valores no **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="217b4-115">This property has as many values as the number of values in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span></span> <span data-ttu-id="217b4-116">Cada valor binário representa um mês e corresponde ao valor no mesmo índice no **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="217b4-116">Each binary value represents a month and corresponds to the value at the same index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span> <span data-ttu-id="217b4-117">Os valores binários são classificados na mesma ordem como os valores no **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="217b4-117">The binary values are sorted in the same order as the values in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span>
  
<span data-ttu-id="217b4-118">Cada valor binário tem um ou mais blocos de 4 bytes, e cada um deles contém nos primeiros dois bytes, a hora de início e hora de término nos dois bytes segundo no formato pouco-endian.</span><span class="sxs-lookup"><span data-stu-id="217b4-118">Each binary value has one or more 4-BYTE blocks and each of them contains the start time in the first two bytes and end time in the second two bytes in little-endian format.</span></span> <span data-ttu-id="217b4-119">A hora de início é o número de minutos entre meia-noite Tempo Universal Coordenado (UTC) do primeiro dia do mês e a hora de início do evento em UTC.</span><span class="sxs-lookup"><span data-stu-id="217b4-119">The start time is the number of minutes between midnight Coordinated Universal Time (UTC) of the first day of the month and the start time of the event in UTC.</span></span> <span data-ttu-id="217b4-120">A hora de término é o número de minutos entre meia-noite UTC do primeiro dia do mês e a hora de término do evento em UTC.</span><span class="sxs-lookup"><span data-stu-id="217b4-120">The end time is the number of minutes between midnight UTC of the first day of the month and the end time of the event in UTC.</span></span> <span data-ttu-id="217b4-121">Os blocos de 4 bytes são classificados em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="217b4-121">The 4-BYTE blocks are sorted in ascending order.</span></span>
  
<span data-ttu-id="217b4-122">Blocos consecutivos ou sobreposição de tempo são mesclados em um bloco com a hora de início como a hora de início do primeiro bloco e hora de término, como o bloco de última hora de término.</span><span class="sxs-lookup"><span data-stu-id="217b4-122">Consecutive or overlapping blocks of time are merged into one block with start time as the start time of the first block and end time as the end time of the last block.</span></span> <span data-ttu-id="217b4-123">Se um evento é espalhado por vários meses ou anos, o evento é dividido em vários blocos, um para cada mês.</span><span class="sxs-lookup"><span data-stu-id="217b4-123">If an event is spread across multiple months or years, the event is split into multiple blocks, one for each month.</span></span> <span data-ttu-id="217b4-124">Se não houver nenhum evento provisório do intervalo de publicação, esta propriedade e **PR_SCHDINFO_MONTHS_TENTATIVE** não devem ser definido ou devem ser excluídos se eles já existirem.</span><span class="sxs-lookup"><span data-stu-id="217b4-124">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_MONTHS_TENTATIVE** must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="217b4-125">Caso contrário, essa propriedade deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="217b4-125">Otherwise, this property must be set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="217b4-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="217b4-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="217b4-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="217b4-127">Protocol specifications</span></span>

<span data-ttu-id="217b4-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="217b4-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="217b4-129">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="217b4-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="217b4-130">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="217b4-130">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="217b4-131">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="217b4-131">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="217b4-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="217b4-132">Header files</span></span>

<span data-ttu-id="217b4-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="217b4-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="217b4-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="217b4-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="217b4-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="217b4-135">Mapitags.h</span></span>
  
> <span data-ttu-id="217b4-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="217b4-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="217b4-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="217b4-137">See also</span></span>



[<span data-ttu-id="217b4-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="217b4-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="217b4-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="217b4-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="217b4-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="217b4-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="217b4-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="217b4-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

