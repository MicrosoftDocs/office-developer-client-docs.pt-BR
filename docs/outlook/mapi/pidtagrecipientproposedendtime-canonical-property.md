---
title: Propriedade canônica PidTagRecipientProposedEndTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedEndTime
api_type:
- COM
ms.assetid: 08dc1f81-964b-4059-9167-e517391b26e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6ea6d634b0e69cf6895c076815941754ba5e83a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332771"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a><span data-ttu-id="0e8ea-103">Propriedade canônica PidTagRecipientProposedEndTime</span><span class="sxs-lookup"><span data-stu-id="0e8ea-103">PidTagRecipientProposedEndTime Canonical Property</span></span>

  
  
<span data-ttu-id="0e8ea-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e8ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e8ea-105">Indica uma hora de término proposta de uma reunião.</span><span class="sxs-lookup"><span data-stu-id="0e8ea-105">Indicates a proposed end time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e8ea-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0e8ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e8ea-107">PR_RECIPIENT_PROPOSEDENDTIME</span><span class="sxs-lookup"><span data-stu-id="0e8ea-107">PR_RECIPIENT_PROPOSEDENDTIME</span></span>  <br/> |
|<span data-ttu-id="0e8ea-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0e8ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e8ea-109">0x5FE4</span><span class="sxs-lookup"><span data-stu-id="0e8ea-109">0x5FE4</span></span>  <br/> |
|<span data-ttu-id="0e8ea-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0e8ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e8ea-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="0e8ea-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="0e8ea-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0e8ea-112">Area:</span></span>  <br/> |<span data-ttu-id="0e8ea-113">Destinatário de transporte</span><span class="sxs-lookup"><span data-stu-id="0e8ea-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e8ea-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e8ea-114">Remarks</span></span>

<span data-ttu-id="0e8ea-115">Quando o valor da propriedade **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) é definido como TRUE, o valor dessa propriedade indica o valor solicitado pelo participante para definir como o valor da propriedade **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) para o objeto de reunião de instância única ou objeto de exceção.</span><span class="sxs-lookup"><span data-stu-id="0e8ea-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e8ea-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e8ea-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e8ea-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0e8ea-117">Protocol specifications</span></span>

<span data-ttu-id="0e8ea-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e8ea-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e8ea-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0e8ea-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e8ea-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e8ea-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e8ea-121">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="0e8ea-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e8ea-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="0e8ea-122">Header files</span></span>

<span data-ttu-id="0e8ea-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e8ea-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e8ea-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0e8ea-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e8ea-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e8ea-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0e8ea-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0e8ea-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e8ea-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e8ea-127">See also</span></span>



[<span data-ttu-id="0e8ea-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0e8ea-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e8ea-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0e8ea-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e8ea-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0e8ea-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e8ea-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0e8ea-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

