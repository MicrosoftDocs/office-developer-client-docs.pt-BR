---
title: Propriedade canônica PidLidAppointmentColor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1ea0830a06f303da8243f927e4a07cc744951ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345434"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="9f9e6-103">Propriedade canônica PidLidAppointmentColor</span><span class="sxs-lookup"><span data-stu-id="9f9e6-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="9f9e6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f9e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f9e6-105">Especifica a cor a ser usada ao exibir o calendário.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f9e6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9f9e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f9e6-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="9f9e6-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="9f9e6-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="9f9e6-108">Property set:</span></span>  <br/> |<span data-ttu-id="9f9e6-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="9f9e6-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="9f9e6-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9f9e6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9f9e6-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="9f9e6-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="9f9e6-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9f9e6-112">Data type:</span></span>  <br/> |<span data-ttu-id="9f9e6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9f9e6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9f9e6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9f9e6-114">Area:</span></span>  <br/> |<span data-ttu-id="9f9e6-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="9f9e6-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f9e6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f9e6-116">Remarks</span></span>

<span data-ttu-id="9f9e6-117">Essa propriedade especifica a cor a ser usada ao exibir o calendário.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="9f9e6-118">Um cliente ou servidor deve definir esse valor para compatibilidade com versões mais antigas.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="9f9e6-119">Em vez disso, ele pode exibir o calendário com base no valor da propriedade **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)), conforme especificado em [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f9e6-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="9f9e6-120">Quando definido, o valor deve ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="9f9e6-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9f9e6-121">**Value**</span></span>|<span data-ttu-id="9f9e6-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="9f9e6-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f9e6-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9f9e6-123">0x00000000</span></span>  <br/> |<span data-ttu-id="9f9e6-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9f9e6-124">None</span></span>  <br/> |
|<span data-ttu-id="9f9e6-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9f9e6-125">0x00000001</span></span>  <br/> |<span data-ttu-id="9f9e6-126">Vermelho</span><span class="sxs-lookup"><span data-stu-id="9f9e6-126">Red</span></span>  <br/> |
|<span data-ttu-id="9f9e6-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9f9e6-127">0x00000002</span></span>  <br/> |<span data-ttu-id="9f9e6-128">Azul</span><span class="sxs-lookup"><span data-stu-id="9f9e6-128">Blue</span></span>  <br/> |
|<span data-ttu-id="9f9e6-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="9f9e6-129">0x00000003</span></span>  <br/> |<span data-ttu-id="9f9e6-130">Verde</span><span class="sxs-lookup"><span data-stu-id="9f9e6-130">Green</span></span>  <br/> |
|<span data-ttu-id="9f9e6-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9f9e6-131">0x00000004</span></span>  <br/> |<span data-ttu-id="9f9e6-132">Cinza</span><span class="sxs-lookup"><span data-stu-id="9f9e6-132">Grey</span></span>  <br/> |
|<span data-ttu-id="9f9e6-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="9f9e6-133">0x00000005</span></span>  <br/> |<span data-ttu-id="9f9e6-134">Laranja</span><span class="sxs-lookup"><span data-stu-id="9f9e6-134">Orange</span></span>  <br/> |
|<span data-ttu-id="9f9e6-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="9f9e6-135">0x00000006</span></span>  <br/> |<span data-ttu-id="9f9e6-136">Ciano</span><span class="sxs-lookup"><span data-stu-id="9f9e6-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="9f9e6-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="9f9e6-137">0x00000007</span></span>  <br/> |<span data-ttu-id="9f9e6-138">Verde-oliva</span><span class="sxs-lookup"><span data-stu-id="9f9e6-138">Olive</span></span>  <br/> |
|<span data-ttu-id="9f9e6-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9f9e6-139">0x00000008</span></span>  <br/> |<span data-ttu-id="9f9e6-140">Roxo</span><span class="sxs-lookup"><span data-stu-id="9f9e6-140">Purple</span></span>  <br/> |
|<span data-ttu-id="9f9e6-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="9f9e6-141">0x00000009</span></span>  <br/> |<span data-ttu-id="9f9e6-142">Azul-petróleo</span><span class="sxs-lookup"><span data-stu-id="9f9e6-142">Teal</span></span>  <br/> |
|<span data-ttu-id="9f9e6-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="9f9e6-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="9f9e6-144">Amarelo</span><span class="sxs-lookup"><span data-stu-id="9f9e6-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9f9e6-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f9e6-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f9e6-146">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9f9e6-146">Protocol specifications</span></span>

<span data-ttu-id="9f9e6-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f9e6-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f9e6-148">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f9e6-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f9e6-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f9e6-150">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f9e6-151">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="9f9e6-151">Header files</span></span>

<span data-ttu-id="9f9e6-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9f9e6-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f9e6-153">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9f9e6-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f9e6-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f9e6-154">See also</span></span>



[<span data-ttu-id="9f9e6-155">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9f9e6-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f9e6-156">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9f9e6-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f9e6-157">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9f9e6-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f9e6-158">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9f9e6-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

