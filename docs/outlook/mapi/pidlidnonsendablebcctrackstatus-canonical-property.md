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
ms.openlocfilehash: e5c795f15046bcab40abc2396b36e14925d3869d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386940"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="31022-103">Propriedade canônica PidLidNonSendableBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="31022-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="31022-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31022-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31022-105">Contém o valor para cada participante que está listado na propriedade **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31022-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31022-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="31022-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31022-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="31022-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="31022-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="31022-108">Property set:</span></span>  <br/> |<span data-ttu-id="31022-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="31022-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="31022-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="31022-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="31022-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="31022-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="31022-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="31022-112">Data type:</span></span>  <br/> |<span data-ttu-id="31022-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="31022-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="31022-114">Área:</span><span class="sxs-lookup"><span data-stu-id="31022-114">Area:</span></span>  <br/> |<span data-ttu-id="31022-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="31022-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31022-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="31022-116">Remarks</span></span>

<span data-ttu-id="31022-117">Essa propriedade é obrigatória somente quando a propriedade **dispidNonSendableBCC** estiver definida.</span><span class="sxs-lookup"><span data-stu-id="31022-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="31022-118">O número de valores desta propriedade deve ser igual o número de valores no **dispidNonSendableBCC**.</span><span class="sxs-lookup"><span data-stu-id="31022-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="31022-119">Cada valor nessa propriedade corresponde ao participante na propriedade **dispidNonSendableBCC** no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="31022-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="31022-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="31022-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="31022-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="31022-121">Protocol specifications</span></span>

<span data-ttu-id="31022-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31022-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31022-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="31022-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="31022-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31022-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31022-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="31022-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="31022-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31022-126">Header files</span></span>

<span data-ttu-id="31022-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31022-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="31022-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="31022-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31022-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="31022-129">See also</span></span>



[<span data-ttu-id="31022-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="31022-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31022-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="31022-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31022-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="31022-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31022-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="31022-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

