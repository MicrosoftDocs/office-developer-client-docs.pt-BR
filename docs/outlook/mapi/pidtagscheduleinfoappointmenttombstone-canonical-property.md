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
ms.openlocfilehash: e554a496dd1869dd7c07b315d92a136676e05006
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590040"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="fa351-103">Propriedade canônica PidTagScheduleInfoAppointmentTombstone</span><span class="sxs-lookup"><span data-stu-id="fa351-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="fa351-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa351-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa351-105">Contém uma lista de blocos de dados que representam as reuniões que tenham sido recusadas.</span><span class="sxs-lookup"><span data-stu-id="fa351-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa351-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fa351-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa351-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="fa351-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="fa351-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fa351-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa351-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="fa351-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="fa351-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fa351-110">Data type:</span></span>  <br/> |<span data-ttu-id="fa351-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fa351-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fa351-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fa351-112">Area:</span></span>  <br/> |<span data-ttu-id="fa351-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="fa351-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa351-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa351-114">Remarks</span></span>

<span data-ttu-id="fa351-115">Os blocos de dados começam com um cabeçalho de valores de 32 bits definido como:</span><span class="sxs-lookup"><span data-stu-id="fa351-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="fa351-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fa351-116">**Value**</span></span>|<span data-ttu-id="fa351-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fa351-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa351-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="fa351-118">Identifier</span></span>  <br/> |<span data-ttu-id="fa351-119">Este campo deve ser o valor 0xBEDEAFCD.</span><span class="sxs-lookup"><span data-stu-id="fa351-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="fa351-120">HeaderSize</span><span class="sxs-lookup"><span data-stu-id="fa351-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="fa351-121">Este campo deve ter o valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="fa351-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="fa351-122">Versão</span><span class="sxs-lookup"><span data-stu-id="fa351-122">Version</span></span>  <br/> |<span data-ttu-id="fa351-123">Este campo deve ter o valor 3.</span><span class="sxs-lookup"><span data-stu-id="fa351-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="fa351-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="fa351-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="fa351-125">A contagem de registros que seguem.</span><span class="sxs-lookup"><span data-stu-id="fa351-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="fa351-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="fa351-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="fa351-127">Este campo deve ter o valor 0x00000014.</span><span class="sxs-lookup"><span data-stu-id="fa351-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="fa351-128">O cabeçalho é seguido por entradas **RecordsCount** dos valores de 32 bits definidos como:</span><span class="sxs-lookup"><span data-stu-id="fa351-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="fa351-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fa351-129">**Value**</span></span>|<span data-ttu-id="fa351-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fa351-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa351-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="fa351-131">StartTime</span></span>  <br/> |<span data-ttu-id="fa351-132">Hora de início do objeto reunião em minutos, desde a meia-noite, dia 1 de janeiro de 1601 UTC.</span><span class="sxs-lookup"><span data-stu-id="fa351-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="fa351-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="fa351-133">EndTime</span></span>  <br/> |<span data-ttu-id="fa351-134">Hora de término do objeto reunião em minutos, desde a meia-noite, dia 1 de janeiro de 1601 UTC.</span><span class="sxs-lookup"><span data-stu-id="fa351-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="fa351-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="fa351-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="fa351-136">O tamanho, em bytes, do campo GlobalObjectId.</span><span class="sxs-lookup"><span data-stu-id="fa351-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="fa351-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="fa351-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="fa351-138">O valor da propriedade **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) da reunião nesse registro representa.</span><span class="sxs-lookup"><span data-stu-id="fa351-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="fa351-139">UserName</span><span class="sxs-lookup"><span data-stu-id="fa351-139">UserName</span></span>  <br/> |<span data-ttu-id="fa351-140">Os dois primeiros bytes são o comprimento da cadeia de caracteres PT_STRING8 que segue.</span><span class="sxs-lookup"><span data-stu-id="fa351-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fa351-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa351-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa351-142">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fa351-142">Protocol specifications</span></span>

<span data-ttu-id="fa351-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa351-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa351-144">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fa351-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa351-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa351-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa351-146">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="fa351-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa351-147">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fa351-147">Header files</span></span>

<span data-ttu-id="fa351-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa351-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa351-149">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fa351-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa351-150">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fa351-150">Mapitags.h</span></span>
  
> <span data-ttu-id="fa351-151">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fa351-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa351-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa351-152">See also</span></span>



[<span data-ttu-id="fa351-153">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fa351-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa351-154">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fa351-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa351-155">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fa351-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa351-156">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fa351-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

