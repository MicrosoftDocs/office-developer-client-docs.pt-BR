---
title: Propriedade canônica PidTagScheduleInfoMonthsAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsAway
api_type:
- COM
ms.assetid: 282a8ba1-b786-4d17-b6c5-17e935e59a6b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 90df272a70fd4133a780f205c93b42f26ed1ae96
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392288"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="af670-103">Propriedade canônica PidTagScheduleInfoMonthsAway</span><span class="sxs-lookup"><span data-stu-id="af670-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="af670-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af670-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af670-105">Contém uma lista dos meses para os quais informações de disponibilidade de dados de tipo de ausência temporária (OOF) estão presentes na mensagem de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="af670-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af670-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="af670-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af670-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="af670-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="af670-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="af670-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af670-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="af670-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="af670-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="af670-110">Data type:</span></span>  <br/> |<span data-ttu-id="af670-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="af670-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="af670-112">Área:</span><span class="sxs-lookup"><span data-stu-id="af670-112">Area:</span></span>  <br/> |<span data-ttu-id="af670-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="af670-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af670-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="af670-114">Remarks</span></span>

<span data-ttu-id="af670-115">O formato, a computação e restrições dessa propriedade são iguais aos de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mas se referir a compromissos que são marcados ausência temporária (OOF) sobre o associado objeto Calendar.</span><span class="sxs-lookup"><span data-stu-id="af670-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af670-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="af670-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af670-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="af670-117">Protocol specifications</span></span>

<span data-ttu-id="af670-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af670-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af670-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="af670-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af670-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af670-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af670-121">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="af670-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af670-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="af670-122">Header files</span></span>

<span data-ttu-id="af670-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af670-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="af670-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="af670-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="af670-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af670-125">Mapitags.h</span></span>
  
> <span data-ttu-id="af670-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="af670-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af670-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="af670-127">See also</span></span>



[<span data-ttu-id="af670-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="af670-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af670-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="af670-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af670-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="af670-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af670-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="af670-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

