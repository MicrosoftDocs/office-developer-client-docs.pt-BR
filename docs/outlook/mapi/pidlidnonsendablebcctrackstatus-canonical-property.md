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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359945"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="d99e0-103">Propriedade canônica PidLidNonSendableBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="d99e0-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="d99e0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d99e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d99e0-105">Contém o valor para cada participante listado na **propriedade dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d99e0-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d99e0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d99e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d99e0-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="d99e0-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="d99e0-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="d99e0-108">Property set:</span></span>  <br/> |<span data-ttu-id="d99e0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d99e0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d99e0-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d99e0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d99e0-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="d99e0-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="d99e0-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d99e0-112">Data type:</span></span>  <br/> |<span data-ttu-id="d99e0-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="d99e0-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="d99e0-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d99e0-114">Area:</span></span>  <br/> |<span data-ttu-id="d99e0-115">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="d99e0-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d99e0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d99e0-116">Remarks</span></span>

<span data-ttu-id="d99e0-117">Essa propriedade é necessária somente quando a **propriedade dispidNonSendableBCC** está definida.</span><span class="sxs-lookup"><span data-stu-id="d99e0-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="d99e0-118">O número de valores nesta propriedade deve ser igual ao número de valores no **dispidNonSendableBCC**.</span><span class="sxs-lookup"><span data-stu-id="d99e0-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="d99e0-119">Cada valor nessa propriedade corresponde ao participante na **propriedade dispidNonSendableBCC** no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="d99e0-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d99e0-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d99e0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d99e0-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d99e0-121">Protocol specifications</span></span>

<span data-ttu-id="d99e0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d99e0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d99e0-123">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d99e0-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d99e0-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d99e0-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d99e0-125">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="d99e0-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d99e0-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="d99e0-126">Header files</span></span>

<span data-ttu-id="d99e0-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d99e0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d99e0-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d99e0-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d99e0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d99e0-129">See also</span></span>



[<span data-ttu-id="d99e0-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d99e0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d99e0-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d99e0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d99e0-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d99e0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d99e0-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d99e0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

