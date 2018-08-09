---
title: Propriedade canônica PidLidReminderDelta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderDelta
api_type:
- COM
ms.assetid: 011d73d0-8b38-4a4e-a56f-92dec451946a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e2caccf3cf6ca7e6f15bed1c901d4dfbb198f19b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768595"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="239cf-103">Propriedade canônica PidLidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="239cf-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="239cf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="239cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="239cf-105">Especifica o intervalo, em minutos, entre o momento em que quando o lembrete primeiro estiver vencido e a hora de início do objeto calendar.</span><span class="sxs-lookup"><span data-stu-id="239cf-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="239cf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="239cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="239cf-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="239cf-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="239cf-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="239cf-108">Property set:</span></span>  <br/> |<span data-ttu-id="239cf-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="239cf-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="239cf-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="239cf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="239cf-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="239cf-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="239cf-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="239cf-112">Data type:</span></span>  <br/> |<span data-ttu-id="239cf-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="239cf-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="239cf-114">Área:</span><span class="sxs-lookup"><span data-stu-id="239cf-114">Area:</span></span>  <br/> |<span data-ttu-id="239cf-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="239cf-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="239cf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="239cf-116">Remarks</span></span>

<span data-ttu-id="239cf-117">Esta propriedade deve ser definida em objetos de calendário.</span><span class="sxs-lookup"><span data-stu-id="239cf-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="239cf-118">Para todos os objetos não são do calendário, essa propriedade deverá ser definida como "0x00000000" e é ignorada.</span><span class="sxs-lookup"><span data-stu-id="239cf-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="239cf-119">Quando um lembrete é descartado para uma instância de um objeto de calendário recorrente, o valor dessa propriedade é usado no cálculo do tempo sinal para a próxima instância.</span><span class="sxs-lookup"><span data-stu-id="239cf-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="239cf-120">Consulte [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) para obter detalhes sobre a criação do objeto de calendário.</span><span class="sxs-lookup"><span data-stu-id="239cf-120">See [[MS- OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="239cf-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="239cf-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="239cf-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="239cf-122">Protocol specifications</span></span>

<span data-ttu-id="239cf-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="239cf-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="239cf-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="239cf-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="239cf-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="239cf-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="239cf-126">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="239cf-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="239cf-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="239cf-127">Header files</span></span>

<span data-ttu-id="239cf-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="239cf-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="239cf-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="239cf-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="239cf-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="239cf-130">See also</span></span>



[<span data-ttu-id="239cf-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="239cf-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="239cf-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="239cf-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="239cf-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="239cf-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="239cf-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="239cf-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

