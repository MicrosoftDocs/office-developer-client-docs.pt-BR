---
title: Propriedade canônica PidLidForwardInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0c32a60c7655f4e468a03013cb3979bde228ea3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768477"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="feef4-103">Propriedade canônica PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="feef4-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="feef4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="feef4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="feef4-105">Indica que a solicitação de reunião representa uma exceção a uma série recorrente, e ele foi encaminhado (mesmo quando encaminhadas pelo organizador) em vez de ser um convite enviado pelo organizador.</span><span class="sxs-lookup"><span data-stu-id="feef4-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="feef4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="feef4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="feef4-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="feef4-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="feef4-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="feef4-108">Property set:</span></span>  <br/> |<span data-ttu-id="feef4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="feef4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="feef4-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="feef4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="feef4-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="feef4-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="feef4-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="feef4-112">Data type:</span></span>  <br/> |<span data-ttu-id="feef4-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="feef4-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="feef4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="feef4-114">Area:</span></span>  <br/> |<span data-ttu-id="feef4-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="feef4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="feef4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="feef4-116">Remarks</span></span>

<span data-ttu-id="feef4-117">Um valor FALSE para esta propriedade indica que a solicitação de reunião não é uma instância encaminhada.</span><span class="sxs-lookup"><span data-stu-id="feef4-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="feef4-118">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="feef4-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="feef4-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="feef4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="feef4-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="feef4-120">Protocol specifications</span></span>

<span data-ttu-id="feef4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feef4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feef4-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="feef4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="feef4-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feef4-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feef4-124">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="feef4-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="feef4-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="feef4-125">Header files</span></span>

<span data-ttu-id="feef4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="feef4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="feef4-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="feef4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="feef4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="feef4-128">See also</span></span>



[<span data-ttu-id="feef4-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="feef4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="feef4-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="feef4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="feef4-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="feef4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="feef4-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="feef4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
