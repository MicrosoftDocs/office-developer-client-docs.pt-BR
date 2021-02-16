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
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="d7b55-103">Propriedade canônica PidTagScheduleInfoAppointmentTombstone</span><span class="sxs-lookup"><span data-stu-id="d7b55-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="d7b55-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7b55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7b55-105">Contém uma lista de blocos de dados que representam reuniões recusadas.</span><span class="sxs-lookup"><span data-stu-id="d7b55-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7b55-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d7b55-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7b55-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="d7b55-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="d7b55-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d7b55-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7b55-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="d7b55-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="d7b55-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d7b55-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7b55-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d7b55-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d7b55-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d7b55-112">Area:</span></span>  <br/> |<span data-ttu-id="d7b55-113">Livre/Ocupado</span><span class="sxs-lookup"><span data-stu-id="d7b55-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7b55-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7b55-114">Remarks</span></span>

<span data-ttu-id="d7b55-115">Os blocos de dados começam com um header de valores de 32 bits definidos como:</span><span class="sxs-lookup"><span data-stu-id="d7b55-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="d7b55-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d7b55-116">**Value**</span></span>|<span data-ttu-id="d7b55-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d7b55-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7b55-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="d7b55-118">Identifier</span></span>  <br/> |<span data-ttu-id="d7b55-119">Esse campo deve ser o valor 0xBEDEAFCD.</span><span class="sxs-lookup"><span data-stu-id="d7b55-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="d7b55-120">HeaderSize</span><span class="sxs-lookup"><span data-stu-id="d7b55-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="d7b55-121">Esse campo deve ter o valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="d7b55-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="d7b55-122">Versão</span><span class="sxs-lookup"><span data-stu-id="d7b55-122">Version</span></span>  <br/> |<span data-ttu-id="d7b55-123">Esse campo deve ter o valor 3.</span><span class="sxs-lookup"><span data-stu-id="d7b55-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="d7b55-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="d7b55-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="d7b55-125">A contagem de registros a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7b55-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="d7b55-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="d7b55-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="d7b55-127">Esse campo deve ter o valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="d7b55-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="d7b55-128">O header é seguido pelas **entradas RecordsCount** de valores de 32 bits definidos como:</span><span class="sxs-lookup"><span data-stu-id="d7b55-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="d7b55-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d7b55-129">**Value**</span></span>|<span data-ttu-id="d7b55-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d7b55-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7b55-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="d7b55-131">StartTime</span></span>  <br/> |<span data-ttu-id="d7b55-132">A hora de início do objeto de reunião em minutos desde a meia-noite de 1º de janeiro de 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="d7b55-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="d7b55-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="d7b55-133">EndTime</span></span>  <br/> |<span data-ttu-id="d7b55-134">A hora de término do objeto de reunião em minutos desde a meia-noite de 1º de janeiro de 1601, UTC.</span><span class="sxs-lookup"><span data-stu-id="d7b55-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="d7b55-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="d7b55-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="d7b55-136">O tamanho, em bytes, do campo GlobalObjectId.</span><span class="sxs-lookup"><span data-stu-id="d7b55-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="d7b55-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="d7b55-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="d7b55-138">O valor da **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) da reunião que esse registro representa.</span><span class="sxs-lookup"><span data-stu-id="d7b55-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="d7b55-139">UserName</span><span class="sxs-lookup"><span data-stu-id="d7b55-139">UserName</span></span>  <br/> |<span data-ttu-id="d7b55-140">Os dois primeiros bytes são o comprimento da cadeia de caracteres PT_STRING8 seguir.</span><span class="sxs-lookup"><span data-stu-id="d7b55-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d7b55-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7b55-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7b55-142">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d7b55-142">Protocol specifications</span></span>

<span data-ttu-id="d7b55-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7b55-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7b55-144">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d7b55-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7b55-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7b55-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7b55-146">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="d7b55-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7b55-147">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="d7b55-147">Header files</span></span>

<span data-ttu-id="d7b55-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7b55-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7b55-149">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d7b55-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7b55-150">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7b55-150">Mapitags.h</span></span>
  
> <span data-ttu-id="d7b55-151">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d7b55-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7b55-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7b55-152">See also</span></span>



[<span data-ttu-id="d7b55-153">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d7b55-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7b55-154">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d7b55-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7b55-155">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d7b55-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7b55-156">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d7b55-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

