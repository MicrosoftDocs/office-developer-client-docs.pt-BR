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
ms.openlocfilehash: 5d84e9cb693cbe732295ee1891b4219450eb09ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351433"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="49b13-103">Propriedade canônica PidTagProcessed</span><span class="sxs-lookup"><span data-stu-id="49b13-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="49b13-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49b13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49b13-105">Defina como TRUE quando a solicitação de reunião tiver sido processada.</span><span class="sxs-lookup"><span data-stu-id="49b13-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49b13-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="49b13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="49b13-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="49b13-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="49b13-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="49b13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="49b13-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="49b13-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="49b13-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="49b13-110">Data type:</span></span>  <br/> |<span data-ttu-id="49b13-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="49b13-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="49b13-112">Área:</span><span class="sxs-lookup"><span data-stu-id="49b13-112">Area:</span></span>  <br/> |<span data-ttu-id="49b13-113">Calendário</span><span class="sxs-lookup"><span data-stu-id="49b13-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49b13-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="49b13-114">Remarks</span></span>

<span data-ttu-id="49b13-115">Essa propriedade garante que as solicitações de reunião sejam processadas uma vez.</span><span class="sxs-lookup"><span data-stu-id="49b13-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="49b13-116">O criador da solicitação deve definir essa propriedade como FALSE e o receptor deve defini-la como TRUE depois que a solicitação está no calendário.</span><span class="sxs-lookup"><span data-stu-id="49b13-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="49b13-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="49b13-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49b13-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="49b13-118">Protocol specifications</span></span>

<span data-ttu-id="49b13-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49b13-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49b13-120">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="49b13-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49b13-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49b13-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49b13-122">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="49b13-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="49b13-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49b13-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49b13-124">Especifica as propriedades e as operações que são permitidas para os objetos de contato e lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="49b13-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49b13-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="49b13-125">Header files</span></span>

<span data-ttu-id="49b13-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="49b13-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="49b13-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="49b13-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="49b13-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="49b13-128">Mapitags.h</span></span>
  
> <span data-ttu-id="49b13-129">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="49b13-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49b13-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="49b13-130">See also</span></span>



[<span data-ttu-id="49b13-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="49b13-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49b13-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="49b13-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49b13-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="49b13-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49b13-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="49b13-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

