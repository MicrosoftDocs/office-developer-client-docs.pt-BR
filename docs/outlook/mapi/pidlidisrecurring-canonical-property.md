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
ms.openlocfilehash: c21f2885f7e9475c2149e42e2a8d947311916b4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768517"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="22d5c-103">Propriedade canônica PidLidIsRecurring</span><span class="sxs-lookup"><span data-stu-id="22d5c-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="22d5c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22d5c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22d5c-105">Especifica se é ou não o objeto associado a uma série recorrente.</span><span class="sxs-lookup"><span data-stu-id="22d5c-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22d5c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="22d5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22d5c-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="22d5c-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="22d5c-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="22d5c-108">Property set:</span></span>  <br/> |<span data-ttu-id="22d5c-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="22d5c-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="22d5c-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="22d5c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="22d5c-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="22d5c-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="22d5c-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="22d5c-112">Data type:</span></span>  <br/> |<span data-ttu-id="22d5c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="22d5c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="22d5c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="22d5c-114">Area:</span></span>  <br/> |<span data-ttu-id="22d5c-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="22d5c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22d5c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="22d5c-116">Remarks</span></span>

<span data-ttu-id="22d5c-117">Um valor TRUE indica que o objeto representa uma série recorrente ou uma exceção (incluindo uma instância órfão).</span><span class="sxs-lookup"><span data-stu-id="22d5c-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="22d5c-118">Um valor falso, ou a ausência dessa propriedade, indica que o objeto representa uma única instância.</span><span class="sxs-lookup"><span data-stu-id="22d5c-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="22d5c-119">Observe a diferença entre essa propriedade e a propriedade **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="22d5c-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22d5c-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="22d5c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22d5c-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="22d5c-121">Protocol specifications</span></span>

<span data-ttu-id="22d5c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22d5c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22d5c-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="22d5c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22d5c-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22d5c-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22d5c-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="22d5c-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22d5c-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="22d5c-126">Header files</span></span>

<span data-ttu-id="22d5c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22d5c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="22d5c-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="22d5c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22d5c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="22d5c-129">See also</span></span>



[<span data-ttu-id="22d5c-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="22d5c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22d5c-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="22d5c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22d5c-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="22d5c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22d5c-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="22d5c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
