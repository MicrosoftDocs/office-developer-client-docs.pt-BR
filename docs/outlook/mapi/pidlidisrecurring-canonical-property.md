---
title: Propriedade canônica PidLidIsRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390846"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="e8970-103">Propriedade canônica PidLidIsRecurring</span><span class="sxs-lookup"><span data-stu-id="e8970-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="e8970-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8970-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8970-105">Especifica se é ou não o objeto associado a uma série recorrente.</span><span class="sxs-lookup"><span data-stu-id="e8970-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8970-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e8970-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8970-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="e8970-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="e8970-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="e8970-108">Property set:</span></span>  <br/> |<span data-ttu-id="e8970-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="e8970-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="e8970-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="e8970-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e8970-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e8970-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="e8970-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e8970-112">Data type:</span></span>  <br/> |<span data-ttu-id="e8970-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e8970-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e8970-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e8970-114">Area:</span></span>  <br/> |<span data-ttu-id="e8970-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="e8970-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8970-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8970-116">Remarks</span></span>

<span data-ttu-id="e8970-117">Um valor TRUE indica que o objeto representa uma série recorrente ou uma exceção (incluindo uma instância órfão).</span><span class="sxs-lookup"><span data-stu-id="e8970-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="e8970-118">Um valor falso, ou a ausência dessa propriedade, indica que o objeto representa uma única instância.</span><span class="sxs-lookup"><span data-stu-id="e8970-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="e8970-119">Observe a diferença entre essa propriedade e a propriedade **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e8970-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8970-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8970-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e8970-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e8970-121">Protocol specifications</span></span>

<span data-ttu-id="e8970-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8970-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8970-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e8970-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e8970-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8970-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8970-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="e8970-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e8970-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e8970-126">Header files</span></span>

<span data-ttu-id="e8970-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8970-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8970-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e8970-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8970-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8970-129">See also</span></span>



[<span data-ttu-id="e8970-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e8970-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8970-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e8970-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8970-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e8970-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8970-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e8970-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

