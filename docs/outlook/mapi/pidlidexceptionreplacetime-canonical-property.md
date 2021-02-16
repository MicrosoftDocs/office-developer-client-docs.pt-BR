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
ms.openlocfilehash: b364fb91bda7e895b546f9a281ef14ce33b073f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337979"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="610c3-103">Propriedade canônica PidLidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="610c3-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="610c3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="610c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="610c3-105">Especifica a data e a hora dentro do padrão de recorrência que a exceção substituirá.</span><span class="sxs-lookup"><span data-stu-id="610c3-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="610c3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="610c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="610c3-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="610c3-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="610c3-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="610c3-108">Property set:</span></span>  <br/> |<span data-ttu-id="610c3-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="610c3-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="610c3-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="610c3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="610c3-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="610c3-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="610c3-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="610c3-112">Data type:</span></span>  <br/> |<span data-ttu-id="610c3-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="610c3-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="610c3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="610c3-114">Area:</span></span>  <br/> |<span data-ttu-id="610c3-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="610c3-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="610c3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="610c3-116">Remarks</span></span>

<span data-ttu-id="610c3-117">O valor deve ser especificado em UTC (Tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="610c3-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="610c3-118">Essa propriedade permite que o objeto de anexo de exceção seja encontrado para uma instância específica.</span><span class="sxs-lookup"><span data-stu-id="610c3-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="610c3-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="610c3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="610c3-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="610c3-120">Protocol specifications</span></span>

<span data-ttu-id="610c3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="610c3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="610c3-122">Fornece definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="610c3-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="610c3-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="610c3-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="610c3-124">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="610c3-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="610c3-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="610c3-125">Header files</span></span>

<span data-ttu-id="610c3-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="610c3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="610c3-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="610c3-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="610c3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="610c3-128">See also</span></span>



[<span data-ttu-id="610c3-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="610c3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="610c3-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="610c3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="610c3-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="610c3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="610c3-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="610c3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

