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
ms.openlocfilehash: c1096df0eff4b43239978620f4ccf2e9d221095a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769977"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="3dd36-103">Propriedade canônica PidTagScheduleInfoMonthsMerged</span><span class="sxs-lookup"><span data-stu-id="3dd36-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="3dd36-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3dd36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3dd36-105">Contém uma lista dos meses para os dados de disponibilidade do tipo ocupado ou uma ausência temporária (OOF) mensagem está presente na mensagem de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="3dd36-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3dd36-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3dd36-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3dd36-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="3dd36-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="3dd36-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3dd36-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3dd36-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="3dd36-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="3dd36-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3dd36-110">Data type:</span></span>  <br/> |<span data-ttu-id="3dd36-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="3dd36-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="3dd36-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3dd36-112">Area:</span></span>  <br/> |<span data-ttu-id="3dd36-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="3dd36-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3dd36-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dd36-114">Remarks</span></span>

<span data-ttu-id="3dd36-115">Eventos do tipo disponível/ocupado provisório não são incluídos nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="3dd36-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="3dd36-116">O formato da sintaxe/e restrições dessa propriedade são iguais aos de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), mas se referir a compromissos que são marcados ausência temporária ou ocupado no objeto calendário associado.</span><span class="sxs-lookup"><span data-stu-id="3dd36-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3dd36-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3dd36-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3dd36-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3dd36-118">Protocol specifications</span></span>

<span data-ttu-id="3dd36-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3dd36-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3dd36-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3dd36-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3dd36-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3dd36-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3dd36-122">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="3dd36-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3dd36-123">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3dd36-123">Header files</span></span>

<span data-ttu-id="3dd36-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3dd36-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3dd36-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3dd36-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3dd36-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3dd36-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3dd36-127">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3dd36-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3dd36-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dd36-128">See also</span></span>



[<span data-ttu-id="3dd36-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3dd36-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3dd36-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3dd36-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3dd36-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3dd36-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3dd36-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3dd36-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

