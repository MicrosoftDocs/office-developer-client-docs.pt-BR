---
title: Propriedade canônica PidLidExceptionReplaceTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e28bde9571081d61b37f6939a991c11ddeb75a4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566044"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="2d09b-103">Propriedade canônica PidLidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="2d09b-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="2d09b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d09b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d09b-105">Especifica a data e hora em que o padrão de recorrência que substituirá a exceção.</span><span class="sxs-lookup"><span data-stu-id="2d09b-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d09b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2d09b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d09b-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="2d09b-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="2d09b-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="2d09b-108">Property set:</span></span>  <br/> |<span data-ttu-id="2d09b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="2d09b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="2d09b-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="2d09b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2d09b-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="2d09b-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="2d09b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2d09b-112">Data type:</span></span>  <br/> |<span data-ttu-id="2d09b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2d09b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="2d09b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2d09b-114">Area:</span></span>  <br/> |<span data-ttu-id="2d09b-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="2d09b-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d09b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d09b-116">Remarks</span></span>

<span data-ttu-id="2d09b-117">O valor deve ser especificado no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="2d09b-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="2d09b-118">Essa propriedade permite que o objeto exception anexo a ser localizado para uma determinada instância.</span><span class="sxs-lookup"><span data-stu-id="2d09b-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2d09b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d09b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2d09b-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2d09b-120">Protocol specifications</span></span>

<span data-ttu-id="2d09b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d09b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d09b-122">Fornece as definições do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2d09b-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="2d09b-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d09b-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d09b-124">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="2d09b-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2d09b-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2d09b-125">Header files</span></span>

<span data-ttu-id="2d09b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d09b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d09b-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2d09b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d09b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d09b-128">See also</span></span>



[<span data-ttu-id="2d09b-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2d09b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d09b-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2d09b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d09b-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2d09b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d09b-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2d09b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

