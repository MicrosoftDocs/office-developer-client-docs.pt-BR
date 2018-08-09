---
title: Propriedade canônica PidLidReminderSignalTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 375cde94d0ecd989908fccbdd69710c1961fba17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768621"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="fa10f-103">Propriedade canônica PidLidReminderSignalTime</span><span class="sxs-lookup"><span data-stu-id="fa10f-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="fa10f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa10f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa10f-105">Especifica o ponto no tempo quando um lembrete passa do pendentes para atrasados.</span><span class="sxs-lookup"><span data-stu-id="fa10f-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa10f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fa10f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa10f-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="fa10f-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="fa10f-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="fa10f-108">Property set:</span></span>  <br/> |<span data-ttu-id="fa10f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fa10f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fa10f-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="fa10f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fa10f-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="fa10f-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="fa10f-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fa10f-112">Data type:</span></span>  <br/> |<span data-ttu-id="fa10f-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fa10f-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fa10f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fa10f-114">Area:</span></span>  <br/> |<span data-ttu-id="fa10f-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="fa10f-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa10f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa10f-116">Remarks</span></span>

<span data-ttu-id="fa10f-117">Esta propriedade deve ser definida se a propriedade **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) for TRUE.</span><span class="sxs-lookup"><span data-stu-id="fa10f-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="fa10f-118">Os clientes devem definir o valor no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="fa10f-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fa10f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa10f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa10f-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fa10f-120">Protocol specifications</span></span>

<span data-ttu-id="fa10f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa10f-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa10f-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fa10f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa10f-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa10f-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa10f-124">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="fa10f-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa10f-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fa10f-125">Header files</span></span>

<span data-ttu-id="fa10f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa10f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa10f-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fa10f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa10f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa10f-128">See also</span></span>



[<span data-ttu-id="fa10f-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fa10f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa10f-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fa10f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa10f-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fa10f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa10f-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fa10f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

