---
title: Propriedade canônica PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327920"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="b70f8-103">Propriedade canônica PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="b70f8-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="b70f8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b70f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b70f8-105">Contém um valor que indica a opinião do remetente da mensagem sobre a importância de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="b70f8-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b70f8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b70f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b70f8-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="b70f8-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="b70f8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b70f8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b70f8-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="b70f8-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="b70f8-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b70f8-110">Data type:</span></span>  <br/> |<span data-ttu-id="b70f8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b70f8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b70f8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b70f8-112">Area:</span></span>  <br/> |<span data-ttu-id="b70f8-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="b70f8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b70f8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b70f8-114">Remarks</span></span>

<span data-ttu-id="b70f8-115">Essa propriedade e a **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) não devem ser confundidos.</span><span class="sxs-lookup"><span data-stu-id="b70f8-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="b70f8-116">A importância indica um valor para os usuários, enquanto a prioridade indica a ordem ou a velocidade em que a mensagem deve ser enviada pelo software do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b70f8-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="b70f8-117">A prioridade mais alta geralmente indica um custo mais alto.</span><span class="sxs-lookup"><span data-stu-id="b70f8-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="b70f8-118">Geralmente, a maior importância é associada a uma exibição diferente da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b70f8-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="b70f8-119">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b70f8-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="b70f8-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="b70f8-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="b70f8-121">A mensagem tem baixa importância.</span><span class="sxs-lookup"><span data-stu-id="b70f8-121">The message has low importance.</span></span>
    
<span data-ttu-id="b70f8-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="b70f8-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="b70f8-123">A mensagem tem alta importância.</span><span class="sxs-lookup"><span data-stu-id="b70f8-123">The message has high importance.</span></span>
    
<span data-ttu-id="b70f8-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="b70f8-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="b70f8-125">A mensagem tem importância normal.</span><span class="sxs-lookup"><span data-stu-id="b70f8-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b70f8-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b70f8-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b70f8-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b70f8-127">Protocol specifications</span></span>

<span data-ttu-id="b70f8-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b70f8-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b70f8-129">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b70f8-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b70f8-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b70f8-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b70f8-131">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="b70f8-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b70f8-132">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b70f8-132">Header files</span></span>

<span data-ttu-id="b70f8-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b70f8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="b70f8-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b70f8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="b70f8-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b70f8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="b70f8-136">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b70f8-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b70f8-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b70f8-137">See also</span></span>



[<span data-ttu-id="b70f8-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b70f8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b70f8-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b70f8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b70f8-140">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b70f8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b70f8-141">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b70f8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

