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
ms.openlocfilehash: 9f6a67dcff6c74f44bbc64ae8b95f3e0ec284a90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769344"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="1c31f-103">Propriedade canônica PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="1c31f-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="1c31f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c31f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c31f-105">Contém um valor que indica a opinião do remetente da mensagem a importância de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1c31f-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c31f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1c31f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c31f-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="1c31f-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="1c31f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1c31f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c31f-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="1c31f-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="1c31f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1c31f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c31f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1c31f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1c31f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1c31f-112">Area:</span></span>  <br/> |<span data-ttu-id="1c31f-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="1c31f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c31f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c31f-114">Remarks</span></span>

<span data-ttu-id="1c31f-115">Essa propriedade e a propriedade **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) não devem ser confundidos.</span><span class="sxs-lookup"><span data-stu-id="1c31f-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="1c31f-116">Prioridade indica um valor para os usuários, enquanto a prioridade indica a ordem ou a velocidade na qual a mensagem deve ser enviada pelo software do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1c31f-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="1c31f-117">Geralmente, a prioridade mais alta indica um alto custo.</span><span class="sxs-lookup"><span data-stu-id="1c31f-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="1c31f-118">Prioridade mais alta geralmente é associada uma exibição diferentes pela interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1c31f-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="1c31f-119">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="1c31f-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="1c31f-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="1c31f-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="1c31f-121">A mensagem tem baixa importância.</span><span class="sxs-lookup"><span data-stu-id="1c31f-121">The message has low importance.</span></span>
    
<span data-ttu-id="1c31f-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="1c31f-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="1c31f-123">A mensagem tem alta prioridade.</span><span class="sxs-lookup"><span data-stu-id="1c31f-123">The message has high importance.</span></span>
    
<span data-ttu-id="1c31f-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="1c31f-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="1c31f-125">A mensagem tem prioridade normal.</span><span class="sxs-lookup"><span data-stu-id="1c31f-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="1c31f-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c31f-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c31f-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1c31f-127">Protocol specifications</span></span>

<span data-ttu-id="1c31f-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c31f-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c31f-129">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1c31f-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c31f-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c31f-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c31f-131">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="1c31f-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c31f-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1c31f-132">Header files</span></span>

<span data-ttu-id="1c31f-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c31f-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c31f-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1c31f-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c31f-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1c31f-135">Mapitags.h</span></span>
  
> <span data-ttu-id="1c31f-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1c31f-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c31f-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c31f-137">See also</span></span>



[<span data-ttu-id="1c31f-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1c31f-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c31f-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1c31f-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c31f-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1c31f-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c31f-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1c31f-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

