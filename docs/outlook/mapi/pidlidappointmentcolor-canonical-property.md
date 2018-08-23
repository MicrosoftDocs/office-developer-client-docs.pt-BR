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
ms.openlocfilehash: f7dcfe32a5edc6587dfbd1351b61e2b1901e1d28
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579050"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="cb91b-103">Propriedade canônica PidLidAppointmentColor</span><span class="sxs-lookup"><span data-stu-id="cb91b-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="cb91b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb91b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb91b-105">Especifica a cor a ser usada ao exibir o calendário.</span><span class="sxs-lookup"><span data-stu-id="cb91b-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb91b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cb91b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb91b-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="cb91b-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="cb91b-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="cb91b-108">Property set:</span></span>  <br/> |<span data-ttu-id="cb91b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="cb91b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="cb91b-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="cb91b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cb91b-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="cb91b-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="cb91b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cb91b-112">Data type:</span></span>  <br/> |<span data-ttu-id="cb91b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cb91b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cb91b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="cb91b-114">Area:</span></span>  <br/> |<span data-ttu-id="cb91b-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="cb91b-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb91b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb91b-116">Remarks</span></span>

<span data-ttu-id="cb91b-117">Esta propriedade especifica a cor a ser usada ao exibir o calendário.</span><span class="sxs-lookup"><span data-stu-id="cb91b-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="cb91b-118">Um cliente ou servidor deve definir esse valor para manter a compatibilidade com clientes mais antigos.</span><span class="sxs-lookup"><span data-stu-id="cb91b-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="cb91b-119">Em vez disso, ele pode exibir o calendário baseado no valor da propriedade de **palavras-chave** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) como especificado em [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cb91b-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="cb91b-120">Quando definido, o valor deve ser um destes procedimentos.</span><span class="sxs-lookup"><span data-stu-id="cb91b-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="cb91b-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cb91b-121">**Value**</span></span>|<span data-ttu-id="cb91b-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="cb91b-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb91b-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cb91b-123">0x00000000</span></span>  <br/> |<span data-ttu-id="cb91b-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cb91b-124">None</span></span>  <br/> |
|<span data-ttu-id="cb91b-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cb91b-125">0x00000001</span></span>  <br/> |<span data-ttu-id="cb91b-126">Vermelho</span><span class="sxs-lookup"><span data-stu-id="cb91b-126">Red</span></span>  <br/> |
|<span data-ttu-id="cb91b-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cb91b-127">0x00000002</span></span>  <br/> |<span data-ttu-id="cb91b-128">Azul</span><span class="sxs-lookup"><span data-stu-id="cb91b-128">Blue</span></span>  <br/> |
|<span data-ttu-id="cb91b-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="cb91b-129">0x00000003</span></span>  <br/> |<span data-ttu-id="cb91b-130">Verde</span><span class="sxs-lookup"><span data-stu-id="cb91b-130">Green</span></span>  <br/> |
|<span data-ttu-id="cb91b-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="cb91b-131">0x00000004</span></span>  <br/> |<span data-ttu-id="cb91b-132">Cinza</span><span class="sxs-lookup"><span data-stu-id="cb91b-132">Grey</span></span>  <br/> |
|<span data-ttu-id="cb91b-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cb91b-133">0x00000005</span></span>  <br/> |<span data-ttu-id="cb91b-134">Laranja</span><span class="sxs-lookup"><span data-stu-id="cb91b-134">Orange</span></span>  <br/> |
|<span data-ttu-id="cb91b-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="cb91b-135">0x00000006</span></span>  <br/> |<span data-ttu-id="cb91b-136">Ciano</span><span class="sxs-lookup"><span data-stu-id="cb91b-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="cb91b-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="cb91b-137">0x00000007</span></span>  <br/> |<span data-ttu-id="cb91b-138">Verde-oliva</span><span class="sxs-lookup"><span data-stu-id="cb91b-138">Olive</span></span>  <br/> |
|<span data-ttu-id="cb91b-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cb91b-139">0x00000008</span></span>  <br/> |<span data-ttu-id="cb91b-140">Roxo</span><span class="sxs-lookup"><span data-stu-id="cb91b-140">Purple</span></span>  <br/> |
|<span data-ttu-id="cb91b-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="cb91b-141">0x00000009</span></span>  <br/> |<span data-ttu-id="cb91b-142">Azul-petróleo</span><span class="sxs-lookup"><span data-stu-id="cb91b-142">Teal</span></span>  <br/> |
|<span data-ttu-id="cb91b-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="cb91b-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="cb91b-144">Amarelo</span><span class="sxs-lookup"><span data-stu-id="cb91b-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cb91b-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb91b-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb91b-146">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb91b-146">Protocol specifications</span></span>

<span data-ttu-id="cb91b-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb91b-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb91b-148">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="cb91b-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb91b-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb91b-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb91b-150">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="cb91b-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb91b-151">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cb91b-151">Header files</span></span>

<span data-ttu-id="cb91b-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb91b-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb91b-153">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cb91b-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb91b-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb91b-154">See also</span></span>



[<span data-ttu-id="cb91b-155">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb91b-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb91b-156">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cb91b-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb91b-157">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cb91b-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb91b-158">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cb91b-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

