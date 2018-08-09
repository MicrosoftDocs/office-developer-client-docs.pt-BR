---
title: Propriedade canônica PidLidReminderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fd40be7733934002b81482a8bf5cfe8c9ce12313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768627"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="ec688-103">Propriedade canônica PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="ec688-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="ec688-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec688-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec688-105">Especifica se um lembrete é definido no objeto.</span><span class="sxs-lookup"><span data-stu-id="ec688-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec688-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ec688-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec688-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="ec688-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="ec688-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="ec688-108">Property set:</span></span>  <br/> |<span data-ttu-id="ec688-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ec688-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ec688-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="ec688-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ec688-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="ec688-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="ec688-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ec688-112">Data type:</span></span>  <br/> |<span data-ttu-id="ec688-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ec688-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ec688-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ec688-114">Area:</span></span>  <br/> |<span data-ttu-id="ec688-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="ec688-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec688-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec688-116">Remarks</span></span>

<span data-ttu-id="ec688-117">Se um objeto de calendário recorrente tem esta propriedade definida como TRUE, o cliente pode substituir esse valor para exceções.</span><span class="sxs-lookup"><span data-stu-id="ec688-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="ec688-118">Se essa propriedade for FALSE em um objeto de calendário recorrente, lembretes estão desabilitados para a série inteira, incluindo exceções.</span><span class="sxs-lookup"><span data-stu-id="ec688-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="ec688-119">Para objetos de tarefa recorrente, essa propriedade não pode ser substituída por exceções (consulte [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) e [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="ec688-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ec688-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec688-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec688-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ec688-121">Protocol specifications</span></span>

<span data-ttu-id="ec688-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec688-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec688-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ec688-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ec688-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec688-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec688-125">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="ec688-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec688-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ec688-126">Header files</span></span>

<span data-ttu-id="ec688-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec688-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec688-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ec688-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec688-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec688-129">See also</span></span>



[<span data-ttu-id="ec688-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ec688-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec688-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ec688-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec688-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ec688-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec688-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ec688-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

