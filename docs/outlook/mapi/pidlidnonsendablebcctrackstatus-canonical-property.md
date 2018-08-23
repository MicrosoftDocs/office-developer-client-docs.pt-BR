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
ms.openlocfilehash: de3c56e3ed532d8f4c3cff272049384e9c6a3867
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586085"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="bfe44-103">Propriedade canônica PidLidNonSendableBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="bfe44-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="bfe44-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfe44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfe44-105">Contém o valor para cada participante que está listado na propriedade **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bfe44-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfe44-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bfe44-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfe44-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="bfe44-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="bfe44-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="bfe44-108">Property set:</span></span>  <br/> |<span data-ttu-id="bfe44-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bfe44-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bfe44-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="bfe44-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bfe44-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="bfe44-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="bfe44-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bfe44-112">Data type:</span></span>  <br/> |<span data-ttu-id="bfe44-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="bfe44-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="bfe44-114">Área:</span><span class="sxs-lookup"><span data-stu-id="bfe44-114">Area:</span></span>  <br/> |<span data-ttu-id="bfe44-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="bfe44-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfe44-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfe44-116">Remarks</span></span>

<span data-ttu-id="bfe44-117">Essa propriedade é obrigatória somente quando a propriedade **dispidNonSendableBCC** estiver definida.</span><span class="sxs-lookup"><span data-stu-id="bfe44-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="bfe44-118">O número de valores desta propriedade deve ser igual o número de valores no **dispidNonSendableBCC**.</span><span class="sxs-lookup"><span data-stu-id="bfe44-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="bfe44-119">Cada valor nessa propriedade corresponde ao participante na propriedade **dispidNonSendableBCC** no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="bfe44-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bfe44-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfe44-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bfe44-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bfe44-121">Protocol specifications</span></span>

<span data-ttu-id="bfe44-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe44-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe44-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="bfe44-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bfe44-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfe44-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfe44-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="bfe44-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bfe44-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bfe44-126">Header files</span></span>

<span data-ttu-id="bfe44-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bfe44-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfe44-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bfe44-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfe44-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfe44-129">See also</span></span>



[<span data-ttu-id="bfe44-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe44-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfe44-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="bfe44-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfe44-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bfe44-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfe44-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bfe44-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

