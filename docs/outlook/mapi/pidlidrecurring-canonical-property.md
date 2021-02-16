---
title: Propriedade canônica PidLidRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 85e78695a7c4fca5a1e5cd28b0254d4559be0c13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315915"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="0b3b9-103">Propriedade canônica PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="0b3b9-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="0b3b9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b3b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b3b9-105">Especifica se uma mensagem de compromisso é recorrente.</span><span class="sxs-lookup"><span data-stu-id="0b3b9-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b3b9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0b3b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b3b9-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="0b3b9-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="0b3b9-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="0b3b9-108">Property set:</span></span>  <br/> |<span data-ttu-id="0b3b9-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0b3b9-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0b3b9-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0b3b9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0b3b9-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="0b3b9-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="0b3b9-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0b3b9-112">Data type:</span></span>  <br/> |<span data-ttu-id="0b3b9-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0b3b9-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0b3b9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0b3b9-114">Area:</span></span>  <br/> |<span data-ttu-id="0b3b9-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="0b3b9-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b3b9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b3b9-116">Remarks</span></span>

<span data-ttu-id="0b3b9-117">Essa propriedade será TRUE se o compromisso for um compromisso recorrente e será FALSE se não for recorrente.</span><span class="sxs-lookup"><span data-stu-id="0b3b9-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="0b3b9-118">Esta propriedade especifica se o objeto representa ou não uma série recorrente.</span><span class="sxs-lookup"><span data-stu-id="0b3b9-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="0b3b9-119">Um valor TRUE indica que o objeto representa uma série recorrente.</span><span class="sxs-lookup"><span data-stu-id="0b3b9-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="0b3b9-120">Um valor FALSE, ou a ausência dessa propriedade, indica que o objeto representa uma única instância ou uma exceção (incluindo uma instância órfã).</span><span class="sxs-lookup"><span data-stu-id="0b3b9-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="0b3b9-121">Observe a diferença entre essa propriedade e a **propriedade LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0b3b9-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b3b9-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b3b9-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b3b9-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0b3b9-123">Protocol specifications</span></span>

<span data-ttu-id="0b3b9-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b3b9-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b3b9-125">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0b3b9-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b3b9-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b3b9-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b3b9-127">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="0b3b9-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b3b9-128">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="0b3b9-128">Header files</span></span>

<span data-ttu-id="0b3b9-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b3b9-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b3b9-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0b3b9-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b3b9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b3b9-131">See also</span></span>



[<span data-ttu-id="0b3b9-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0b3b9-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b3b9-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0b3b9-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b3b9-134">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0b3b9-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b3b9-135">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0b3b9-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

