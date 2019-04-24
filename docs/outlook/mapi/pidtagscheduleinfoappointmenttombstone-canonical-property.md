---
title: Propriedade canônica PidTagScheduleInfoAppointmentTombstone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321319"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="7af78-103">Propriedade canônica PidTagScheduleInfoAppointmentTombstone</span><span class="sxs-lookup"><span data-stu-id="7af78-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="7af78-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7af78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7af78-105">Contém uma lista de blocos de dados que representam as reuniões que foram recusadas.</span><span class="sxs-lookup"><span data-stu-id="7af78-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7af78-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7af78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7af78-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="7af78-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="7af78-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7af78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7af78-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="7af78-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="7af78-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7af78-110">Data type:</span></span>  <br/> |<span data-ttu-id="7af78-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7af78-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7af78-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7af78-112">Area:</span></span>  <br/> |<span data-ttu-id="7af78-113">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="7af78-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7af78-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7af78-114">Remarks</span></span>

<span data-ttu-id="7af78-115">Os blocos de dados começam com um cabeçalho de valores de 32 bits definidos como:</span><span class="sxs-lookup"><span data-stu-id="7af78-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="7af78-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7af78-116">**Value**</span></span>|<span data-ttu-id="7af78-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7af78-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7af78-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="7af78-118">Identifier</span></span>  <br/> |<span data-ttu-id="7af78-119">Este campo deve ser o valor 0xBEDEAFCD.</span><span class="sxs-lookup"><span data-stu-id="7af78-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="7af78-120">Cabeçalhosize</span><span class="sxs-lookup"><span data-stu-id="7af78-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="7af78-121">Este campo deve ter o valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="7af78-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="7af78-122">Version</span><span class="sxs-lookup"><span data-stu-id="7af78-122">Version</span></span>  <br/> |<span data-ttu-id="7af78-123">Este campo deve ter o valor 3.</span><span class="sxs-lookup"><span data-stu-id="7af78-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="7af78-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="7af78-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="7af78-125">A contagem de registros a seguir.</span><span class="sxs-lookup"><span data-stu-id="7af78-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="7af78-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="7af78-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="7af78-127">Este campo deve ter o valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="7af78-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="7af78-128">O cabeçalho é seguido por entradas **RecordsCount** dos valores de 32 bits definidos como:</span><span class="sxs-lookup"><span data-stu-id="7af78-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="7af78-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7af78-129">**Value**</span></span>|<span data-ttu-id="7af78-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7af78-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7af78-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="7af78-131">StartTime</span></span>  <br/> |<span data-ttu-id="7af78-132">O tempo de início do objeto de reunião em minutos, desde a meia-noite, 1º de janeiro de 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="7af78-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="7af78-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="7af78-133">EndTime</span></span>  <br/> |<span data-ttu-id="7af78-134">O horário de término do objeto de reunião em minutos desde a meia-noite, 1º de janeiro de 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="7af78-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="7af78-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="7af78-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="7af78-136">O tamanho, em bytes, do campo GlobalObjectId.</span><span class="sxs-lookup"><span data-stu-id="7af78-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="7af78-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="7af78-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="7af78-138">O valor da propriedade **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) da reunião que este registro representa.</span><span class="sxs-lookup"><span data-stu-id="7af78-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="7af78-139">UserName</span><span class="sxs-lookup"><span data-stu-id="7af78-139">UserName</span></span>  <br/> |<span data-ttu-id="7af78-140">Os primeiros dois bytes são o comprimento da cadeia de caracteres PT_STRING8 a seguir.</span><span class="sxs-lookup"><span data-stu-id="7af78-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7af78-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7af78-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7af78-142">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="7af78-142">Protocol specifications</span></span>

<span data-ttu-id="7af78-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af78-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7af78-144">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7af78-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7af78-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7af78-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7af78-146">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="7af78-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7af78-147">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7af78-147">Header files</span></span>

<span data-ttu-id="7af78-148">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7af78-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="7af78-149">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7af78-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="7af78-150">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7af78-150">Mapitags.h</span></span>
  
> <span data-ttu-id="7af78-151">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7af78-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7af78-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="7af78-152">See also</span></span>



[<span data-ttu-id="7af78-153">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7af78-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7af78-154">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7af78-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7af78-155">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7af78-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7af78-156">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7af78-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

