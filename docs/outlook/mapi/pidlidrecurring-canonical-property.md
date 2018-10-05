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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399477"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="ca012-103">Propriedade canônica PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="ca012-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="ca012-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca012-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca012-105">Especifica se uma mensagem de compromisso recorrente.</span><span class="sxs-lookup"><span data-stu-id="ca012-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca012-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ca012-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca012-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="ca012-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="ca012-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="ca012-108">Property set:</span></span>  <br/> |<span data-ttu-id="ca012-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ca012-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ca012-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="ca012-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ca012-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="ca012-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="ca012-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ca012-112">Data type:</span></span>  <br/> |<span data-ttu-id="ca012-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ca012-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ca012-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ca012-114">Area:</span></span>  <br/> |<span data-ttu-id="ca012-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="ca012-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca012-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca012-116">Remarks</span></span>

<span data-ttu-id="ca012-117">Essa propriedade é TRUE se o compromisso é um compromisso recorrente e for FALSE, se ela não é recorrente.</span><span class="sxs-lookup"><span data-stu-id="ca012-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="ca012-118">Esta propriedade especifica se ou não o objeto representa uma série recorrente.</span><span class="sxs-lookup"><span data-stu-id="ca012-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="ca012-119">Um valor TRUE indica que o objeto representa uma série recorrente.</span><span class="sxs-lookup"><span data-stu-id="ca012-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="ca012-120">Um valor falso, ou a ausência dessa propriedade, indica que o objeto representa uma única instância ou uma exceção (incluindo uma instância órfão).</span><span class="sxs-lookup"><span data-stu-id="ca012-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="ca012-121">Observe a diferença entre essa propriedade e a propriedade **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ca012-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca012-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca012-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca012-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ca012-123">Protocol specifications</span></span>

<span data-ttu-id="ca012-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca012-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca012-125">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ca012-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca012-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca012-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca012-127">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="ca012-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca012-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ca012-128">Header files</span></span>

<span data-ttu-id="ca012-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca012-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca012-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ca012-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca012-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca012-131">See also</span></span>



[<span data-ttu-id="ca012-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ca012-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca012-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ca012-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca012-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ca012-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca012-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ca012-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

