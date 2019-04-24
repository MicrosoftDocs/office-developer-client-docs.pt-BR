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
# <a name="pidtagrecipientproposedendtime-canonical-property"></a><span data-ttu-id="50239-103">Propriedade canônica PidTagRecipientProposedEndTime</span><span class="sxs-lookup"><span data-stu-id="50239-103">PidTagRecipientProposedEndTime Canonical Property</span></span>

  
  
<span data-ttu-id="50239-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50239-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50239-105">Indica a hora de término proposta de uma reunião.</span><span class="sxs-lookup"><span data-stu-id="50239-105">Indicates a proposed end time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50239-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="50239-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50239-107">PR_RECIPIENT_PROPOSEDENDTIME</span><span class="sxs-lookup"><span data-stu-id="50239-107">PR_RECIPIENT_PROPOSEDENDTIME</span></span>  <br/> |
|<span data-ttu-id="50239-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="50239-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50239-109">0x5FE4</span><span class="sxs-lookup"><span data-stu-id="50239-109">0x5FE4</span></span>  <br/> |
|<span data-ttu-id="50239-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="50239-110">Data type:</span></span>  <br/> |<span data-ttu-id="50239-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="50239-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="50239-112">Área:</span><span class="sxs-lookup"><span data-stu-id="50239-112">Area:</span></span>  <br/> |<span data-ttu-id="50239-113">Destinatário de transporte</span><span class="sxs-lookup"><span data-stu-id="50239-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50239-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="50239-114">Remarks</span></span>

<span data-ttu-id="50239-115">Quando o valor da propriedade **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) é definido como true, o valor dessa propriedade indica o valor solicitado pelo participante a ser definido como o valor do **dispidApptEndWhole** ([ PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) propriedade para o objeto de reunião de instância única ou objeto de exceção.</span><span class="sxs-lookup"><span data-stu-id="50239-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50239-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="50239-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50239-117">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="50239-117">Protocol specifications</span></span>

<span data-ttu-id="50239-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50239-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50239-119">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="50239-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50239-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50239-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50239-121">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="50239-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50239-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="50239-122">Header files</span></span>

<span data-ttu-id="50239-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="50239-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="50239-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="50239-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="50239-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="50239-125">Mapitags.h</span></span>
  
> <span data-ttu-id="50239-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="50239-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50239-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="50239-127">See also</span></span>



[<span data-ttu-id="50239-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="50239-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50239-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="50239-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50239-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="50239-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50239-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="50239-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

