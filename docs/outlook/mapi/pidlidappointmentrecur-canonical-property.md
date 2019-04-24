---
title: Propriedade canônica PidLidAppointmentRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331777"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="ce5a3-103">Propriedade canônica PidLidAppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="ce5a3-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="ce5a3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce5a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce5a3-105">Especifica as datas e horas em que uma série recorrente ocorre usando um dos padrões de recorrência e intervalos especificados em [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce5a3-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ce5a3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ce5a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce5a3-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="ce5a3-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="ce5a3-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="ce5a3-108">Property set:</span></span>  <br/> |<span data-ttu-id="ce5a3-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ce5a3-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ce5a3-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ce5a3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ce5a3-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="ce5a3-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="ce5a3-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ce5a3-112">Data type:</span></span>  <br/> |<span data-ttu-id="ce5a3-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ce5a3-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ce5a3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ce5a3-114">Area:</span></span>  <br/> |<span data-ttu-id="ce5a3-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="ce5a3-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce5a3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce5a3-116">Remarks</span></span>

<span data-ttu-id="ce5a3-117">Esta propriedade especifica as datas e horas em que uma série recorrente ocorre usando um dos padrões de recorrência e intervalos detalhados em [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce5a3-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="ce5a3-118">O valor dessa propriedade também contém informações sobre exceções modificadas e excluídas; informações como datas, assunto, local e várias outras propriedades de exceções.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="ce5a3-119">Os dados binários dessa propriedade para itens de calendário recorrentes são armazenados como a estrutura **AppointmentRecurrencePattern** .</span><span class="sxs-lookup"><span data-stu-id="ce5a3-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="ce5a3-120">Esta propriedade não deve existir em itens de calendário de instância única.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="ce5a3-121">Há algumas limitações para recorrências:</span><span class="sxs-lookup"><span data-stu-id="ce5a3-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="ce5a3-122">Várias instâncias não devem começar no mesmo dia.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="ce5a3-123">As ocorrências não devem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-123">Occurrences must not overlap.</span></span> <span data-ttu-id="ce5a3-124">Especificamente, uma exceção que modifica a data de início de uma instância na série recorrente deve ocorrer em uma data que seja após o final da instância anterior e o início da próxima instância na série recorrente.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="ce5a3-125">O mesmo é verdadeiro se as instâncias anterior ou seguinte na série recorrente são exceções.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="ce5a3-126">A agenda de uma série recorrente é determinada por seu padrão e intervalo de recorrência.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ce5a3-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce5a3-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ce5a3-128">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="ce5a3-128">Protocol specifications</span></span>

<span data-ttu-id="ce5a3-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce5a3-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce5a3-130">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ce5a3-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce5a3-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce5a3-132">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="ce5a3-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce5a3-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce5a3-134">Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ce5a3-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ce5a3-135">Header files</span></span>

<span data-ttu-id="ce5a3-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ce5a3-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce5a3-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ce5a3-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce5a3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce5a3-138">See also</span></span>



[<span data-ttu-id="ce5a3-139">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ce5a3-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce5a3-140">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ce5a3-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce5a3-141">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ce5a3-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce5a3-142">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ce5a3-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

