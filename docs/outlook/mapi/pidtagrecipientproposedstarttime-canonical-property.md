---
title: Propriedade canônica PidTagRecipientProposedStartTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedStartTime
api_type:
- COM
ms.assetid: 6687ff62-7ac6-409c-8c87-4e09d38e45f1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 65d5c2f94da219fc1cb87384ebdd3c1cf34bd9a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769779"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="ef0b7-103">Propriedade canônica PidTagRecipientProposedStartTime</span><span class="sxs-lookup"><span data-stu-id="ef0b7-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="ef0b7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef0b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef0b7-105">Indica uma hora de início proposta de uma reunião.</span><span class="sxs-lookup"><span data-stu-id="ef0b7-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef0b7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ef0b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef0b7-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="ef0b7-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="ef0b7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ef0b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef0b7-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="ef0b7-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="ef0b7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ef0b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef0b7-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ef0b7-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ef0b7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ef0b7-112">Area:</span></span>  <br/> |<span data-ttu-id="ef0b7-113">Destinatário de transporte</span><span class="sxs-lookup"><span data-stu-id="ef0b7-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef0b7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef0b7-114">Remarks</span></span>

<span data-ttu-id="ef0b7-115">Quando o valor da propriedade **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) é definido como TRUE, o valor dessa propriedade indica o valor solicitado pelo participante para definir como o valor do **dispidApptStartWhole** ([ PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) a propriedade para o objeto de reunião única instância ou um objeto exception.</span><span class="sxs-lookup"><span data-stu-id="ef0b7-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ef0b7-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef0b7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ef0b7-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ef0b7-117">Protocol specifications</span></span>

<span data-ttu-id="ef0b7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef0b7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef0b7-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ef0b7-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ef0b7-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef0b7-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef0b7-121">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="ef0b7-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ef0b7-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ef0b7-122">Header files</span></span>

<span data-ttu-id="ef0b7-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef0b7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef0b7-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ef0b7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef0b7-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ef0b7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ef0b7-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ef0b7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef0b7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef0b7-127">See also</span></span>



[<span data-ttu-id="ef0b7-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ef0b7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef0b7-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ef0b7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef0b7-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ef0b7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef0b7-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ef0b7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

