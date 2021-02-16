---
title: Propriedade canônica PidTagScheduleInfoFreeBusyAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyAway
api_type:
- COM
ms.assetid: 7b5d013a-15ac-469a-98c8-3ed1e80f6faf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7520c473ee9373f8c23c4f5b4bb020291e2be007
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338504"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="fc26b-103">Propriedade canônica PidTagScheduleInfoFreeBusyAway</span><span class="sxs-lookup"><span data-stu-id="fc26b-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="fc26b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc26b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc26b-105">Contém os horários para os quais o status de livre/ocupado está definido como OOF.</span><span class="sxs-lookup"><span data-stu-id="fc26b-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc26b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fc26b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc26b-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="fc26b-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="fc26b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fc26b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc26b-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="fc26b-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="fc26b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fc26b-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc26b-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="fc26b-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="fc26b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fc26b-112">Area:</span></span>  <br/> |<span data-ttu-id="fc26b-113">Livre/Ocupado</span><span class="sxs-lookup"><span data-stu-id="fc26b-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc26b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc26b-114">Remarks</span></span>

<span data-ttu-id="fc26b-115">O formato, a computação e as restrições dessa propriedade são os mesmos de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mas se referem a compromissos marcados como OOF no calendário associado.</span><span class="sxs-lookup"><span data-stu-id="fc26b-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fc26b-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc26b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc26b-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fc26b-117">Protocol specifications</span></span>

<span data-ttu-id="fc26b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc26b-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc26b-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fc26b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc26b-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc26b-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc26b-121">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="fc26b-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc26b-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="fc26b-122">Header files</span></span>

<span data-ttu-id="fc26b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc26b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc26b-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fc26b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc26b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc26b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fc26b-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fc26b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc26b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc26b-127">See also</span></span>



[<span data-ttu-id="fc26b-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc26b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc26b-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fc26b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc26b-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fc26b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc26b-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fc26b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

