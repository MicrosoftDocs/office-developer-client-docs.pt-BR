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
ms.openlocfilehash: 717f934c0dadc46935b72c409469633e0779fb3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576334"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="67428-103">Propriedade canônica PidTagScheduleInfoFreeBusyAway</span><span class="sxs-lookup"><span data-stu-id="67428-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="67428-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67428-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67428-105">Contém os horários em que o status livre/ocupado é definido como ausência temporária.</span><span class="sxs-lookup"><span data-stu-id="67428-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67428-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="67428-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67428-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="67428-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="67428-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="67428-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67428-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="67428-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="67428-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="67428-110">Data type:</span></span>  <br/> |<span data-ttu-id="67428-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="67428-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="67428-112">Área:</span><span class="sxs-lookup"><span data-stu-id="67428-112">Area:</span></span>  <br/> |<span data-ttu-id="67428-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="67428-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67428-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="67428-114">Remarks</span></span>

<span data-ttu-id="67428-115">O formato, a computação e restrições dessa propriedade são iguais aos de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mas se referir a compromissos que são marcados OOF no calendário associado.</span><span class="sxs-lookup"><span data-stu-id="67428-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="67428-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="67428-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67428-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="67428-117">Protocol specifications</span></span>

<span data-ttu-id="67428-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67428-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67428-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="67428-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67428-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67428-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67428-121">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="67428-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67428-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="67428-122">Header files</span></span>

<span data-ttu-id="67428-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67428-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="67428-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="67428-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="67428-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67428-125">Mapitags.h</span></span>
  
> <span data-ttu-id="67428-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="67428-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67428-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="67428-127">See also</span></span>



[<span data-ttu-id="67428-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="67428-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67428-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="67428-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67428-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="67428-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67428-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="67428-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

