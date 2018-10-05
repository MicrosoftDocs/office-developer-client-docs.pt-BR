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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400828"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="c83af-103">Propriedade canônica PidTagImportance</span><span class="sxs-lookup"><span data-stu-id="c83af-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="c83af-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c83af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c83af-105">Contém um valor que indica a opinião do remetente da mensagem a importância de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c83af-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c83af-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c83af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c83af-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="c83af-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="c83af-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c83af-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c83af-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="c83af-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="c83af-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c83af-110">Data type:</span></span>  <br/> |<span data-ttu-id="c83af-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c83af-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c83af-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c83af-112">Area:</span></span>  <br/> |<span data-ttu-id="c83af-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="c83af-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c83af-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c83af-114">Remarks</span></span>

<span data-ttu-id="c83af-115">Essa propriedade e a propriedade **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) não devem ser confundidos.</span><span class="sxs-lookup"><span data-stu-id="c83af-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="c83af-116">Prioridade indica um valor para os usuários, enquanto a prioridade indica a ordem ou a velocidade na qual a mensagem deve ser enviada pelo software do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c83af-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="c83af-117">Geralmente, a prioridade mais alta indica um alto custo.</span><span class="sxs-lookup"><span data-stu-id="c83af-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="c83af-118">Prioridade mais alta geralmente é associada uma exibição diferentes pela interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c83af-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="c83af-119">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c83af-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="c83af-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="c83af-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="c83af-121">A mensagem tem baixa importância.</span><span class="sxs-lookup"><span data-stu-id="c83af-121">The message has low importance.</span></span>
    
<span data-ttu-id="c83af-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="c83af-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="c83af-123">A mensagem tem alta prioridade.</span><span class="sxs-lookup"><span data-stu-id="c83af-123">The message has high importance.</span></span>
    
<span data-ttu-id="c83af-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="c83af-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="c83af-125">A mensagem tem prioridade normal.</span><span class="sxs-lookup"><span data-stu-id="c83af-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c83af-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c83af-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c83af-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c83af-127">Protocol specifications</span></span>

<span data-ttu-id="c83af-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c83af-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c83af-129">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c83af-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c83af-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c83af-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c83af-131">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="c83af-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c83af-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c83af-132">Header files</span></span>

<span data-ttu-id="c83af-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c83af-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c83af-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c83af-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="c83af-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c83af-135">Mapitags.h</span></span>
  
> <span data-ttu-id="c83af-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c83af-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c83af-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c83af-137">See also</span></span>



[<span data-ttu-id="c83af-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c83af-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c83af-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c83af-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c83af-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c83af-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c83af-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c83af-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

