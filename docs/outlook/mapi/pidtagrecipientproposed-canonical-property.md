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
ms.openlocfilehash: 2e00f121bf52f2c6fcbe797fb8f6126584444411
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580688"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="49d62-103">Propriedade canônica PidTagRecipientProposed</span><span class="sxs-lookup"><span data-stu-id="49d62-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="49d62-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49d62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49d62-105">Indica se um participante da reunião respondeu.</span><span class="sxs-lookup"><span data-stu-id="49d62-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49d62-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="49d62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49d62-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="49d62-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="49d62-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="49d62-108">Identifier:</span></span>  <br/> |<span data-ttu-id="49d62-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="49d62-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="49d62-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="49d62-110">Data type:</span></span>  <br/> |<span data-ttu-id="49d62-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="49d62-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="49d62-112">Área:</span><span class="sxs-lookup"><span data-stu-id="49d62-112">Area:</span></span>  <br/> |<span data-ttu-id="49d62-113">Destinatário de transporte</span><span class="sxs-lookup"><span data-stu-id="49d62-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49d62-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="49d62-114">Remarks</span></span>

<span data-ttu-id="49d62-115">Um valor TRUE para esta propriedade indica que o participante proposta uma nova data / hora.</span><span class="sxs-lookup"><span data-stu-id="49d62-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="49d62-116">Um valor FALSE, ou pela ausência dessa propriedade, significa que o participante não ainda respondeu, ou a resposta mais recente do participante não incluir uma nova data / hora proposta.</span><span class="sxs-lookup"><span data-stu-id="49d62-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="49d62-117">Este valor não deve ser TRUE para participantes em uma série recorrente.</span><span class="sxs-lookup"><span data-stu-id="49d62-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="49d62-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="49d62-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49d62-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="49d62-119">Protocol specifications</span></span>

<span data-ttu-id="49d62-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49d62-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49d62-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="49d62-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49d62-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49d62-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49d62-123">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="49d62-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49d62-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="49d62-124">Header files</span></span>

<span data-ttu-id="49d62-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49d62-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="49d62-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="49d62-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="49d62-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="49d62-127">Mapitags.h</span></span>
  
> <span data-ttu-id="49d62-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="49d62-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49d62-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="49d62-129">See also</span></span>



[<span data-ttu-id="49d62-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="49d62-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49d62-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="49d62-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49d62-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="49d62-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49d62-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="49d62-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

