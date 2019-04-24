---
title: Propriedade canônica PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336474"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="786c2-103">Propriedade canônica PidTagScheduleInfoMonthsMerged</span><span class="sxs-lookup"><span data-stu-id="786c2-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="786c2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="786c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="786c2-105">Contém uma lista dos meses nos quais os dados de disponibilidade do tipo ocupado ou uma mensagem de ausência temporária (OOF) estão presentes na mensagem de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="786c2-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="786c2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="786c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="786c2-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="786c2-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="786c2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="786c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="786c2-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="786c2-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="786c2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="786c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="786c2-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="786c2-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="786c2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="786c2-112">Area:</span></span>  <br/> |<span data-ttu-id="786c2-113">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="786c2-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="786c2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="786c2-114">Remarks</span></span>

<span data-ttu-id="786c2-115">Os eventos da tentativa de tipo de disponibilidade não estão incluídos nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="786c2-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="786c2-116">A sintaxe/o formato e as restrições dessa propriedade são os mesmos do **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), mas se referem aos compromissos marcados como OOF ou inatividade no objeto Calendar associado.</span><span class="sxs-lookup"><span data-stu-id="786c2-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="786c2-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="786c2-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="786c2-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="786c2-118">Protocol specifications</span></span>

<span data-ttu-id="786c2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="786c2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="786c2-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="786c2-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="786c2-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="786c2-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="786c2-122">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="786c2-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="786c2-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="786c2-123">Header files</span></span>

<span data-ttu-id="786c2-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="786c2-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="786c2-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="786c2-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="786c2-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="786c2-126">Mapitags.h</span></span>
  
> <span data-ttu-id="786c2-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="786c2-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="786c2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="786c2-128">See also</span></span>



[<span data-ttu-id="786c2-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="786c2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="786c2-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="786c2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="786c2-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="786c2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="786c2-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="786c2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

