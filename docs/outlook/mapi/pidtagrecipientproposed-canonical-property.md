---
title: Propriedade canônica PidTagRecipientProposed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1b09d8d7621121b3652ceb9824f6d36b53844206
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283132"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="44e12-103">Propriedade canônica PidTagRecipientProposed</span><span class="sxs-lookup"><span data-stu-id="44e12-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="44e12-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44e12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44e12-105">Indica se um participante da reunião respondeu.</span><span class="sxs-lookup"><span data-stu-id="44e12-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44e12-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="44e12-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44e12-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="44e12-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="44e12-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="44e12-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44e12-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="44e12-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="44e12-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="44e12-110">Data type:</span></span>  <br/> |<span data-ttu-id="44e12-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="44e12-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="44e12-112">Área:</span><span class="sxs-lookup"><span data-stu-id="44e12-112">Area:</span></span>  <br/> |<span data-ttu-id="44e12-113">Destinatário de transporte</span><span class="sxs-lookup"><span data-stu-id="44e12-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44e12-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="44e12-114">Remarks</span></span>

<span data-ttu-id="44e12-115">Um valor TRUE para essa propriedade indica que o participante proposto uma nova data e/ou hora.</span><span class="sxs-lookup"><span data-stu-id="44e12-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="44e12-116">Um valor FALSO, ou a ausência dessa propriedade, significa que o participante ainda não respondeu ou a resposta mais recente do participante não incluiu uma nova proposta de data/hora.</span><span class="sxs-lookup"><span data-stu-id="44e12-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="44e12-117">Esse valor não deve ser VERDADEIRO para os participantes de uma série recorrente.</span><span class="sxs-lookup"><span data-stu-id="44e12-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="44e12-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="44e12-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44e12-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="44e12-119">Protocol specifications</span></span>

<span data-ttu-id="44e12-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44e12-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44e12-121">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="44e12-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44e12-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44e12-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44e12-123">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="44e12-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44e12-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="44e12-124">Header files</span></span>

<span data-ttu-id="44e12-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44e12-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="44e12-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="44e12-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="44e12-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44e12-127">Mapitags.h</span></span>
  
> <span data-ttu-id="44e12-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="44e12-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44e12-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="44e12-129">See also</span></span>



[<span data-ttu-id="44e12-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="44e12-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44e12-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="44e12-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44e12-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="44e12-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44e12-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="44e12-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

