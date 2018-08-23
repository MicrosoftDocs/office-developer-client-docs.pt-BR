---
title: Propriedade canônica PidLidNonSendToTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cf9d11b7a53ee0b9911e32cb3c3e2a0a490e4729
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592784"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="5c327-103">Propriedade canônica PidLidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="5c327-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="5c327-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c327-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c327-105">Contém o valor para cada participante listado na propriedade **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5c327-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c327-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5c327-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c327-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="5c327-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="5c327-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="5c327-108">Property set:</span></span>  <br/> |<span data-ttu-id="5c327-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5c327-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5c327-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="5c327-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5c327-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="5c327-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="5c327-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5c327-112">Data type:</span></span>  <br/> |<span data-ttu-id="5c327-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="5c327-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="5c327-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5c327-114">Area:</span></span>  <br/> |<span data-ttu-id="5c327-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="5c327-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c327-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c327-116">Remarks</span></span>

<span data-ttu-id="5c327-117">Essa propriedade é obrigatória somente quando a propriedade **dispidNonSendableTo** estiver definida.</span><span class="sxs-lookup"><span data-stu-id="5c327-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="5c327-118">O número de valores desta propriedade deve ser igual ao número de valores em **dispidNonSendableTo**.</span><span class="sxs-lookup"><span data-stu-id="5c327-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="5c327-119">Cada valor PT_LONG essa propriedade corresponde do participante na propriedade **dispidNonSendableTo** no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="5c327-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5c327-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c327-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c327-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5c327-121">Protocol specifications</span></span>

<span data-ttu-id="5c327-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c327-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c327-123">Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5c327-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c327-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c327-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c327-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="5c327-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c327-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5c327-126">Header files</span></span>

<span data-ttu-id="5c327-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c327-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c327-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5c327-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c327-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c327-129">See also</span></span>



[<span data-ttu-id="5c327-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5c327-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c327-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5c327-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c327-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5c327-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c327-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5c327-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

