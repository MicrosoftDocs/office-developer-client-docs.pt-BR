---
title: Propriedade canônica PidLidReminderTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382467"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="5329f-103">Propriedade canônica PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="5329f-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="5329f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5329f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5329f-105">Especifica a hora de sinal inicial de um lembrete.</span><span class="sxs-lookup"><span data-stu-id="5329f-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5329f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5329f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5329f-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="5329f-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="5329f-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="5329f-108">Property set:</span></span>  <br/> |<span data-ttu-id="5329f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5329f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5329f-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="5329f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5329f-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="5329f-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="5329f-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5329f-112">Data type:</span></span>  <br/> |<span data-ttu-id="5329f-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5329f-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5329f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5329f-114">Area:</span></span>  <br/> |<span data-ttu-id="5329f-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="5329f-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5329f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5329f-116">Remarks</span></span>

<span data-ttu-id="5329f-117">Para objetos de calendário, essa propriedade representa a hora de quando o usuário seria tardia, que é a hora de início do compromisso.</span><span class="sxs-lookup"><span data-stu-id="5329f-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="5329f-118">Os clientes devem definir o valor no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="5329f-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5329f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5329f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5329f-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5329f-120">Protocol specifications</span></span>

<span data-ttu-id="5329f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5329f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5329f-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5329f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5329f-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5329f-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5329f-124">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="5329f-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5329f-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5329f-125">Header files</span></span>

<span data-ttu-id="5329f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5329f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5329f-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5329f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5329f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5329f-128">See also</span></span>



[<span data-ttu-id="5329f-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5329f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5329f-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5329f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5329f-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5329f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5329f-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5329f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

