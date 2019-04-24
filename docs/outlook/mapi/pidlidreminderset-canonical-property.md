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
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335151"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="fc271-103">Propriedade canônica PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="fc271-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="fc271-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc271-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc271-105">Especifica se um lembrete está definido no objeto.</span><span class="sxs-lookup"><span data-stu-id="fc271-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc271-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fc271-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc271-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="fc271-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="fc271-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="fc271-108">Property set:</span></span>  <br/> |<span data-ttu-id="fc271-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fc271-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fc271-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fc271-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fc271-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="fc271-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="fc271-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fc271-112">Data type:</span></span>  <br/> |<span data-ttu-id="fc271-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fc271-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fc271-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fc271-114">Area:</span></span>  <br/> |<span data-ttu-id="fc271-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="fc271-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc271-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc271-116">Remarks</span></span>

<span data-ttu-id="fc271-117">Se um objeto Calendar recorrente tiver essa propriedade definida como TRUE, o cliente poderá substituir esse valor por exceções.</span><span class="sxs-lookup"><span data-stu-id="fc271-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="fc271-118">Se essa propriedade for FALSE em um objeto Calendar recorrente, lembretes serão desabilitados para toda a série, incluindo exceções.</span><span class="sxs-lookup"><span data-stu-id="fc271-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="fc271-119">Para objetos de tarefa recorrentes, essa propriedade não pode ser substituída por exceções (consulte [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) e [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="fc271-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fc271-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc271-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc271-121">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="fc271-121">Protocol specifications</span></span>

<span data-ttu-id="fc271-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc271-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc271-123">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fc271-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc271-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc271-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc271-125">Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.</span><span class="sxs-lookup"><span data-stu-id="fc271-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc271-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fc271-126">Header files</span></span>

<span data-ttu-id="fc271-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fc271-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc271-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fc271-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc271-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc271-129">See also</span></span>



[<span data-ttu-id="fc271-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc271-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc271-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fc271-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc271-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fc271-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc271-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fc271-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

