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
ms.openlocfilehash: 585e1a5400965288aa4a4c321888a570270021c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357768"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="5edb6-103">Propriedade canônica PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="5edb6-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="5edb6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5edb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5edb6-105">Indica que a solicitação de reunião representa uma exceção a uma série recorrente e foi encaminhada (mesmo quando encaminhada pelo organizador) em vez de ser um convite enviado pelo organizador.</span><span class="sxs-lookup"><span data-stu-id="5edb6-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5edb6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5edb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5edb6-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="5edb6-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="5edb6-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="5edb6-108">Property set:</span></span>  <br/> |<span data-ttu-id="5edb6-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5edb6-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5edb6-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5edb6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5edb6-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="5edb6-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="5edb6-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5edb6-112">Data type:</span></span>  <br/> |<span data-ttu-id="5edb6-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5edb6-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5edb6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5edb6-114">Area:</span></span>  <br/> |<span data-ttu-id="5edb6-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="5edb6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5edb6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5edb6-116">Remarks</span></span>

<span data-ttu-id="5edb6-117">Um valor FALSE para esta propriedade indica que a solicitação de reunião não é uma instância encaminhada.</span><span class="sxs-lookup"><span data-stu-id="5edb6-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="5edb6-118">Esta propriedade não é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="5edb6-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5edb6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5edb6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5edb6-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="5edb6-120">Protocol specifications</span></span>

<span data-ttu-id="5edb6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5edb6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5edb6-122">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5edb6-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5edb6-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5edb6-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5edb6-124">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="5edb6-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5edb6-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5edb6-125">Header files</span></span>

<span data-ttu-id="5edb6-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5edb6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5edb6-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5edb6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5edb6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5edb6-128">See also</span></span>



[<span data-ttu-id="5edb6-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5edb6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5edb6-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5edb6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5edb6-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5edb6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5edb6-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5edb6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

