---
title: Propriedade canônica PidLidReminderFileParameter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderFileParameter
api_type:
- COM
ms.assetid: 1009f0ea-6f35-484d-b04d-5b6e844c14dd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1cfb8f7070a8001e94fa70e90c52635c9b8be122
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768614"
---
# <a name="pidlidreminderfileparameter-canonical-property"></a><span data-ttu-id="ee242-103">Propriedade canônica PidLidReminderFileParameter</span><span class="sxs-lookup"><span data-stu-id="ee242-103">PidLidReminderFileParameter Canonical Property</span></span>

  
  
<span data-ttu-id="ee242-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee242-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee242-105">Especifica o nome de arquivo do som que um cliente deve executar quando o lembrete para aquele objeto estiver vencido.</span><span class="sxs-lookup"><span data-stu-id="ee242-105">Specifies the filename of the sound that a client should play when the reminder for that object becomes overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee242-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ee242-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee242-107">dispidReminderFileParam</span><span class="sxs-lookup"><span data-stu-id="ee242-107">dispidReminderFileParam</span></span>  <br/> |
|<span data-ttu-id="ee242-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="ee242-108">Property set:</span></span>  <br/> |<span data-ttu-id="ee242-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ee242-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ee242-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="ee242-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ee242-111">0x0000851F</span><span class="sxs-lookup"><span data-stu-id="ee242-111">0x0000851F</span></span>  <br/> |
|<span data-ttu-id="ee242-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ee242-112">Data type:</span></span>  <br/> |<span data-ttu-id="ee242-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee242-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee242-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ee242-114">Area:</span></span>  <br/> |<span data-ttu-id="ee242-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="ee242-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee242-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee242-116">Remarks</span></span>

<span data-ttu-id="ee242-117">Se essa propriedade não estiver presente, o cliente pode usar um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="ee242-117">If this property is not present, the client may use a default value.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ee242-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee242-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee242-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ee242-119">Protocol specifications</span></span>

<span data-ttu-id="ee242-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee242-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee242-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ee242-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee242-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee242-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee242-123">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="ee242-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee242-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ee242-124">Header files</span></span>

<span data-ttu-id="ee242-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee242-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee242-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ee242-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee242-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee242-127">See also</span></span>



[<span data-ttu-id="ee242-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ee242-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee242-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ee242-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee242-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ee242-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee242-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ee242-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

