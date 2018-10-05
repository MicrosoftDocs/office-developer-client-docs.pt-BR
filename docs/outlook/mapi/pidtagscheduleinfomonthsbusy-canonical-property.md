---
title: Propriedade canônica PidTagScheduleInfoMonthsBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b15447d6-89aa-40ad-93fc-21fbfa5e3d0e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 08f8f6e016ff08211bc10e80588ab33e83d6441b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393849"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a><span data-ttu-id="00ddb-103">Propriedade canônica PidTagScheduleInfoMonthsBusy</span><span class="sxs-lookup"><span data-stu-id="00ddb-103">PidTagScheduleInfoMonthsBusy Canonical Property</span></span>

  
  
<span data-ttu-id="00ddb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00ddb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00ddb-105">Contém os meses para os quais informações de disponibilidade de dados do tipo ocupado estão presentes na mensagem de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="00ddb-105">Contains the months for which free/busy data of type busy is present in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00ddb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="00ddb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00ddb-107">PR_SCHDINFO_MONTHS_BUSY</span><span class="sxs-lookup"><span data-stu-id="00ddb-107">PR_SCHDINFO_MONTHS_BUSY</span></span>  <br/> |
|<span data-ttu-id="00ddb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="00ddb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00ddb-109">0x6853</span><span class="sxs-lookup"><span data-stu-id="00ddb-109">0x6853</span></span>  <br/> |
|<span data-ttu-id="00ddb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="00ddb-110">Data type:</span></span>  <br/> |<span data-ttu-id="00ddb-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="00ddb-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="00ddb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="00ddb-112">Area:</span></span>  <br/> |<span data-ttu-id="00ddb-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="00ddb-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00ddb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="00ddb-114">Remarks</span></span>

<span data-ttu-id="00ddb-115">O formato, a computação e restrições dessa propriedade são iguais aos de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), mas se referir a compromissos que são marcados ocorrendo no objeto calendário associado.</span><span class="sxs-lookup"><span data-stu-id="00ddb-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="00ddb-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="00ddb-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00ddb-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="00ddb-117">Protocol specifications</span></span>

<span data-ttu-id="00ddb-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00ddb-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00ddb-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="00ddb-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00ddb-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00ddb-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00ddb-121">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="00ddb-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00ddb-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="00ddb-122">Header files</span></span>

<span data-ttu-id="00ddb-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00ddb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="00ddb-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="00ddb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="00ddb-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00ddb-125">Mapitags.h</span></span>
  
> <span data-ttu-id="00ddb-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="00ddb-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00ddb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="00ddb-127">See also</span></span>



[<span data-ttu-id="00ddb-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="00ddb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00ddb-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="00ddb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00ddb-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="00ddb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00ddb-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="00ddb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

