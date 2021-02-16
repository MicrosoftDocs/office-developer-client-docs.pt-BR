---
title: Propriedade canônica PidTagScheduleInfoFreeBusyMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyMerged
api_type:
- COM
ms.assetid: 3ebfccb6-967a-4f8e-9d94-94c50ba65438
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338714"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="2d4d6-103">Propriedade canônica PidTagScheduleInfoFreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="2d4d6-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="2d4d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d4d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d4d6-105">Contém os horários para os quais o status de ocupado está definido como ocupado ou OOF.</span><span class="sxs-lookup"><span data-stu-id="2d4d6-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d4d6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2d4d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d4d6-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="2d4d6-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="2d4d6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2d4d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2d4d6-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="2d4d6-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="2d4d6-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2d4d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="2d4d6-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d4d6-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="2d4d6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2d4d6-112">Area:</span></span>  <br/> |<span data-ttu-id="2d4d6-113">Livre/Ocupado</span><span class="sxs-lookup"><span data-stu-id="2d4d6-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d4d6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d4d6-114">Remarks</span></span>

<span data-ttu-id="2d4d6-115">Eventos provisórios de tipo de ocupado/livre não são incluídos nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="2d4d6-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="2d4d6-116">O formato, a computação e as restrições dessa propriedade são iguais às do **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mas se referem a compromissos marcados como OOF ou ocupado no calendário associado.</span><span class="sxs-lookup"><span data-stu-id="2d4d6-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2d4d6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d4d6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2d4d6-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2d4d6-118">Protocol specifications</span></span>

<span data-ttu-id="2d4d6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d4d6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d4d6-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2d4d6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2d4d6-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d4d6-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d4d6-122">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="2d4d6-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2d4d6-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="2d4d6-123">Header files</span></span>

<span data-ttu-id="2d4d6-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d4d6-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d4d6-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2d4d6-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="2d4d6-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2d4d6-126">Mapitags.h</span></span>
  
> <span data-ttu-id="2d4d6-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2d4d6-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d4d6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d4d6-128">See also</span></span>



[<span data-ttu-id="2d4d6-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2d4d6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d4d6-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2d4d6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d4d6-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2d4d6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d4d6-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2d4d6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

