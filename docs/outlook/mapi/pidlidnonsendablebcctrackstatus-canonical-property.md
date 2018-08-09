---
title: Propriedade canônica PidLidNonSendableBccTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da2bd4e87c7076872ccff708983cfbe631b27122
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768540"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="19806-103">Propriedade canônica PidLidNonSendableBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="19806-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="19806-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19806-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19806-105">Contém o valor para cada participante que está listado na propriedade **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="19806-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19806-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="19806-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19806-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="19806-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="19806-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="19806-108">Property set:</span></span>  <br/> |<span data-ttu-id="19806-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="19806-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="19806-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="19806-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="19806-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="19806-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="19806-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="19806-112">Data type:</span></span>  <br/> |<span data-ttu-id="19806-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="19806-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="19806-114">Área:</span><span class="sxs-lookup"><span data-stu-id="19806-114">Area:</span></span>  <br/> |<span data-ttu-id="19806-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="19806-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19806-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="19806-116">Remarks</span></span>

<span data-ttu-id="19806-117">Essa propriedade é obrigatória somente quando a propriedade **dispidNonSendableBCC** estiver definida.</span><span class="sxs-lookup"><span data-stu-id="19806-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="19806-118">O número de valores desta propriedade deve ser igual o número de valores no **dispidNonSendableBCC**.</span><span class="sxs-lookup"><span data-stu-id="19806-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="19806-119">Cada valor nessa propriedade corresponde ao participante na propriedade **dispidNonSendableBCC** no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="19806-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="19806-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="19806-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19806-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="19806-121">Protocol specifications</span></span>

<span data-ttu-id="19806-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19806-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19806-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="19806-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19806-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19806-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19806-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="19806-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19806-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="19806-126">Header files</span></span>

<span data-ttu-id="19806-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19806-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="19806-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="19806-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19806-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="19806-129">See also</span></span>



[<span data-ttu-id="19806-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="19806-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19806-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="19806-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19806-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="19806-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19806-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="19806-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

