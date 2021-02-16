---
title: Propriedade canônica PidTagSwappedToDoStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358902"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="2aa60-103">Propriedade canônica PidTagSwappedToDoStore</span><span class="sxs-lookup"><span data-stu-id="2aa60-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="2aa60-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aa60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aa60-105">Determina a necessidade de processamento pós-transmissão de um email.</span><span class="sxs-lookup"><span data-stu-id="2aa60-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2aa60-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2aa60-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2aa60-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="2aa60-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="2aa60-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2aa60-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2aa60-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="2aa60-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="2aa60-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2aa60-110">Data type:</span></span>  <br/> |<span data-ttu-id="2aa60-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2aa60-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2aa60-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2aa60-112">Area:</span></span>  <br/> |<span data-ttu-id="2aa60-113">MAPI não transmitível</span><span class="sxs-lookup"><span data-stu-id="2aa60-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2aa60-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2aa60-114">Remarks</span></span>

<span data-ttu-id="2aa60-115">Se essa propriedade for definida em uma mensagem de rascunho, seu valor deverá ser definido como o valor da propriedade **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2aa60-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="2aa60-116">Para obter mais informações, consulte a seção [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) "Pós-transmissão de processamento de uma mensagem sinalizada".</span><span class="sxs-lookup"><span data-stu-id="2aa60-116">For more information, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2aa60-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2aa60-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2aa60-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2aa60-118">Protocol specifications</span></span>

<span data-ttu-id="2aa60-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2aa60-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2aa60-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2aa60-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2aa60-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2aa60-121">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2aa60-122">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="2aa60-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="2aa60-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2aa60-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2aa60-124">Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.</span><span class="sxs-lookup"><span data-stu-id="2aa60-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2aa60-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="2aa60-125">Header files</span></span>

<span data-ttu-id="2aa60-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2aa60-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2aa60-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2aa60-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2aa60-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2aa60-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2aa60-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2aa60-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2aa60-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2aa60-130">See also</span></span>



[<span data-ttu-id="2aa60-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2aa60-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2aa60-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2aa60-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2aa60-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2aa60-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2aa60-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2aa60-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

