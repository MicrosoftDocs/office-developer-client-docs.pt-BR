---
title: Propriedade canônica PidTagProcessed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProcessed
api_type:
- COM
ms.assetid: 44884f60-7e36-45b2-9712-4f9821a0dc1f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0918f079769a70aa11e4f26551ec232308e5eef0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769679"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="45c58-103">Propriedade canônica PidTagProcessed</span><span class="sxs-lookup"><span data-stu-id="45c58-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="45c58-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45c58-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45c58-105">Defina como TRUE quando a solicitação de reunião foi processada.</span><span class="sxs-lookup"><span data-stu-id="45c58-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45c58-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="45c58-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45c58-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="45c58-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="45c58-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="45c58-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45c58-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="45c58-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="45c58-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="45c58-110">Data type:</span></span>  <br/> |<span data-ttu-id="45c58-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="45c58-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="45c58-112">Área:</span><span class="sxs-lookup"><span data-stu-id="45c58-112">Area:</span></span>  <br/> |<span data-ttu-id="45c58-113">Calendário</span><span class="sxs-lookup"><span data-stu-id="45c58-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45c58-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="45c58-114">Remarks</span></span>

<span data-ttu-id="45c58-115">Esta propriedade garante que as solicitações de reunião obtém processadas uma vez.</span><span class="sxs-lookup"><span data-stu-id="45c58-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="45c58-116">O criador da solicitação deve definir essa propriedade como FALSE e o receptor deve defini-la como TRUE assim que a solicitação do calendário.</span><span class="sxs-lookup"><span data-stu-id="45c58-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45c58-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45c58-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45c58-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="45c58-118">Protocol specifications</span></span>

<span data-ttu-id="45c58-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c58-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c58-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="45c58-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45c58-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c58-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c58-122">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="45c58-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="45c58-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45c58-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45c58-124">Especifica as propriedades e operações que são permitidas para contato e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="45c58-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45c58-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45c58-125">Header files</span></span>

<span data-ttu-id="45c58-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45c58-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="45c58-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="45c58-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="45c58-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45c58-128">Mapitags.h</span></span>
  
> <span data-ttu-id="45c58-129">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="45c58-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45c58-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="45c58-130">See also</span></span>



[<span data-ttu-id="45c58-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45c58-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45c58-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="45c58-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45c58-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="45c58-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45c58-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="45c58-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

