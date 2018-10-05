---
title: Propriedade canônica PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385449"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="d88bb-103">Propriedade canônica PidTagPriority</span><span class="sxs-lookup"><span data-stu-id="d88bb-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="d88bb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d88bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d88bb-105">Contém a prioridade relativa de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d88bb-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d88bb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d88bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d88bb-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="d88bb-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="d88bb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d88bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d88bb-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="d88bb-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="d88bb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d88bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="d88bb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d88bb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d88bb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d88bb-112">Area:</span></span>  <br/> |<span data-ttu-id="d88bb-113">Email</span><span class="sxs-lookup"><span data-stu-id="d88bb-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d88bb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d88bb-114">Remarks</span></span>

<span data-ttu-id="d88bb-115">Essa propriedade e a propriedade **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) não devem ser confundidos.</span><span class="sxs-lookup"><span data-stu-id="d88bb-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="d88bb-116">Prioridade indica um valor para os usuários, enquanto a prioridade indica a ordem ou a velocidade na qual a mensagem deve ser enviada pelo software do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d88bb-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="d88bb-117">Geralmente, a prioridade mais alta indica um alto custo.</span><span class="sxs-lookup"><span data-stu-id="d88bb-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="d88bb-118">Prioridade mais alta geralmente é associada uma exibição diferentes pela interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d88bb-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="d88bb-119">A prioridade de uma mensagem de relatório deve ser o mesmo que a prioridade da mensagem original serem reportada.</span><span class="sxs-lookup"><span data-stu-id="d88bb-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="d88bb-120">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d88bb-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="d88bb-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="d88bb-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="d88bb-122">A mensagem não é urgente.</span><span class="sxs-lookup"><span data-stu-id="d88bb-122">The message is not urgent.</span></span>
    
<span data-ttu-id="d88bb-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="d88bb-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="d88bb-124">A mensagem tem prioridade normal.</span><span class="sxs-lookup"><span data-stu-id="d88bb-124">The message has normal priority.</span></span>
    
<span data-ttu-id="d88bb-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="d88bb-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="d88bb-126">A mensagem é urgente.</span><span class="sxs-lookup"><span data-stu-id="d88bb-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d88bb-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d88bb-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d88bb-128">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d88bb-128">Protocol specifications</span></span>

<span data-ttu-id="d88bb-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d88bb-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d88bb-130">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d88bb-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d88bb-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d88bb-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d88bb-132">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d88bb-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d88bb-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d88bb-133">Header files</span></span>

<span data-ttu-id="d88bb-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d88bb-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="d88bb-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d88bb-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="d88bb-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d88bb-136">Mapitags.h</span></span>
  
> <span data-ttu-id="d88bb-137">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d88bb-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d88bb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d88bb-138">See also</span></span>



[<span data-ttu-id="d88bb-139">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d88bb-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d88bb-140">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d88bb-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d88bb-141">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d88bb-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d88bb-142">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d88bb-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

