---
title: Propriedade canônica PidLidNonSendCcTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1ee68f0f60f96798130115cbd313f6d7cd403486
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590495"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="3ee24-103">Propriedade canônica PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="3ee24-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="3ee24-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ee24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ee24-105">Contém o valor para cada participante listado na propriedade **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3ee24-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ee24-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3ee24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3ee24-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="3ee24-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="3ee24-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="3ee24-108">Property set:</span></span>  <br/> |<span data-ttu-id="3ee24-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="3ee24-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3ee24-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="3ee24-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3ee24-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="3ee24-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="3ee24-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3ee24-112">Data type:</span></span>  <br/> |<span data-ttu-id="3ee24-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="3ee24-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="3ee24-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3ee24-114">Area:</span></span>  <br/> |<span data-ttu-id="3ee24-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="3ee24-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ee24-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ee24-116">Remarks</span></span>

<span data-ttu-id="3ee24-117">Essa propriedade é obrigatória somente quando a propriedade **dispidNonSendableCC** estiver definida.</span><span class="sxs-lookup"><span data-stu-id="3ee24-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="3ee24-118">O número de valores desta propriedade deve ser igual ao número de valores em **dispidNonSendableCC**.</span><span class="sxs-lookup"><span data-stu-id="3ee24-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="3ee24-119">Cada valor PT_LONG essa propriedade corresponde do participante na propriedade **dispidNonSendableCC** no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="3ee24-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3ee24-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ee24-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3ee24-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3ee24-121">Protocol specifications</span></span>

<span data-ttu-id="3ee24-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ee24-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ee24-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ee24-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3ee24-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ee24-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ee24-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="3ee24-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3ee24-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3ee24-126">Header files</span></span>

<span data-ttu-id="3ee24-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ee24-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3ee24-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3ee24-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ee24-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ee24-129">See also</span></span>



[<span data-ttu-id="3ee24-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3ee24-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3ee24-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3ee24-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3ee24-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3ee24-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3ee24-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3ee24-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

