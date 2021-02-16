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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303406"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="17d35-103">Propriedade canônica PidTagScheduleInfoMonthsAway</span><span class="sxs-lookup"><span data-stu-id="17d35-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="17d35-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17d35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17d35-105">Contém uma lista dos meses para os quais os dados de livre/ocupado de tipo de escritório (OOF) estão presentes na mensagem de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="17d35-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17d35-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="17d35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17d35-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="17d35-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="17d35-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="17d35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17d35-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="17d35-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="17d35-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="17d35-110">Data type:</span></span>  <br/> |<span data-ttu-id="17d35-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="17d35-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="17d35-112">Área:</span><span class="sxs-lookup"><span data-stu-id="17d35-112">Area:</span></span>  <br/> |<span data-ttu-id="17d35-113">Livre/Ocupado</span><span class="sxs-lookup"><span data-stu-id="17d35-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17d35-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="17d35-114">Remarks</span></span>

<span data-ttu-id="17d35-115">O formato, a computação e as restrições dessa propriedade são os mesmos de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mas se referem a compromissos que estão marcados como fora do escritório (OOF) no objeto de calendário associado.</span><span class="sxs-lookup"><span data-stu-id="17d35-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="17d35-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="17d35-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17d35-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="17d35-117">Protocol specifications</span></span>

<span data-ttu-id="17d35-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17d35-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17d35-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="17d35-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17d35-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17d35-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17d35-121">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="17d35-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17d35-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="17d35-122">Header files</span></span>

<span data-ttu-id="17d35-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17d35-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="17d35-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="17d35-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="17d35-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17d35-125">Mapitags.h</span></span>
  
> <span data-ttu-id="17d35-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="17d35-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17d35-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="17d35-127">See also</span></span>



[<span data-ttu-id="17d35-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="17d35-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17d35-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="17d35-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17d35-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="17d35-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17d35-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="17d35-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

