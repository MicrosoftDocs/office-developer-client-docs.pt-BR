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
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="61339-103">Propriedade canônica PidLidAppointmentColor</span><span class="sxs-lookup"><span data-stu-id="61339-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="61339-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61339-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61339-105">Especifica a cor a ser usada ao exibir o calendário.</span><span class="sxs-lookup"><span data-stu-id="61339-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61339-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="61339-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61339-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="61339-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="61339-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="61339-108">Property set:</span></span>  <br/> |<span data-ttu-id="61339-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="61339-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="61339-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="61339-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="61339-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="61339-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="61339-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="61339-112">Data type:</span></span>  <br/> |<span data-ttu-id="61339-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="61339-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="61339-114">Área:</span><span class="sxs-lookup"><span data-stu-id="61339-114">Area:</span></span>  <br/> |<span data-ttu-id="61339-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="61339-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61339-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="61339-116">Remarks</span></span>

<span data-ttu-id="61339-117">Esta propriedade especifica a cor a ser usada ao exibir o calendário.</span><span class="sxs-lookup"><span data-stu-id="61339-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="61339-118">Um cliente ou servidor deve definir esse valor para compatibilidade com versões anteriores de clientes mais antigos.</span><span class="sxs-lookup"><span data-stu-id="61339-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="61339-119">Em vez disso, ele pode exibir o calendário com base no \*\*\*\* valor da Propriedade Keywords ([PidNameKeywords](pidnamekeywords-canonical-property.md)) conforme especificado em [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="61339-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="61339-120">Quando definido, o valor deve ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="61339-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="61339-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="61339-121">**Value**</span></span>|<span data-ttu-id="61339-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="61339-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61339-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61339-123">0x00000000</span></span>  <br/> |<span data-ttu-id="61339-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="61339-124">None</span></span>  <br/> |
|<span data-ttu-id="61339-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="61339-125">0x00000001</span></span>  <br/> |<span data-ttu-id="61339-126">Vermelho</span><span class="sxs-lookup"><span data-stu-id="61339-126">Red</span></span>  <br/> |
|<span data-ttu-id="61339-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="61339-127">0x00000002</span></span>  <br/> |<span data-ttu-id="61339-128">Azul</span><span class="sxs-lookup"><span data-stu-id="61339-128">Blue</span></span>  <br/> |
|<span data-ttu-id="61339-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="61339-129">0x00000003</span></span>  <br/> |<span data-ttu-id="61339-130">Verde</span><span class="sxs-lookup"><span data-stu-id="61339-130">Green</span></span>  <br/> |
|<span data-ttu-id="61339-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="61339-131">0x00000004</span></span>  <br/> |<span data-ttu-id="61339-132">Cinza</span><span class="sxs-lookup"><span data-stu-id="61339-132">Grey</span></span>  <br/> |
|<span data-ttu-id="61339-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="61339-133">0x00000005</span></span>  <br/> |<span data-ttu-id="61339-134">Laranja</span><span class="sxs-lookup"><span data-stu-id="61339-134">Orange</span></span>  <br/> |
|<span data-ttu-id="61339-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="61339-135">0x00000006</span></span>  <br/> |<span data-ttu-id="61339-136">Ciano</span><span class="sxs-lookup"><span data-stu-id="61339-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="61339-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="61339-137">0x00000007</span></span>  <br/> |<span data-ttu-id="61339-138">Verde-oliva</span><span class="sxs-lookup"><span data-stu-id="61339-138">Olive</span></span>  <br/> |
|<span data-ttu-id="61339-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="61339-139">0x00000008</span></span>  <br/> |<span data-ttu-id="61339-140">Roxo</span><span class="sxs-lookup"><span data-stu-id="61339-140">Purple</span></span>  <br/> |
|<span data-ttu-id="61339-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="61339-141">0x00000009</span></span>  <br/> |<span data-ttu-id="61339-142">Azul-petróleo</span><span class="sxs-lookup"><span data-stu-id="61339-142">Teal</span></span>  <br/> |
|<span data-ttu-id="61339-143">Interrupção</span><span class="sxs-lookup"><span data-stu-id="61339-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="61339-144">Amarelo</span><span class="sxs-lookup"><span data-stu-id="61339-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="61339-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="61339-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="61339-146">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="61339-146">Protocol specifications</span></span>

<span data-ttu-id="61339-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61339-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61339-148">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="61339-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="61339-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61339-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61339-150">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="61339-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="61339-151">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61339-151">Header files</span></span>

<span data-ttu-id="61339-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="61339-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="61339-153">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="61339-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61339-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="61339-154">See also</span></span>



[<span data-ttu-id="61339-155">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="61339-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61339-156">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="61339-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61339-157">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="61339-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61339-158">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="61339-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

