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
ms.openlocfilehash: cbe1915df46010c5574065826ac1814f45c8c093
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770144"
---
# <a name="pidtagswappedtodostore-canonical-property"></a><span data-ttu-id="8a048-103">Propriedade canônica PidTagSwappedToDoStore</span><span class="sxs-lookup"><span data-stu-id="8a048-103">PidTagSwappedToDoStore Canonical Property</span></span>

  
  
<span data-ttu-id="8a048-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a048-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a048-105">Determina a necessidade para pós-transmitir processamento de um email.</span><span class="sxs-lookup"><span data-stu-id="8a048-105">Determines the need for post-transmit processing of an email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a048-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8a048-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a048-107">PR_SWAPPED_TODO_STORE</span><span class="sxs-lookup"><span data-stu-id="8a048-107">PR_SWAPPED_TODO_STORE</span></span>  <br/> |
|<span data-ttu-id="8a048-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8a048-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a048-109">0x0E2C</span><span class="sxs-lookup"><span data-stu-id="8a048-109">0x0E2C</span></span>  <br/> |
|<span data-ttu-id="8a048-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8a048-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a048-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8a048-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8a048-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8a048-112">Area:</span></span>  <br/> |<span data-ttu-id="8a048-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="8a048-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a048-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a048-114">Remarks</span></span>

<span data-ttu-id="8a048-115">Se essa propriedade for definida em uma mensagem de rascunho, seu valor deve ser definido como o valor da propriedade **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8a048-115">If this property is set on a draft message, then its value must be set to the value of **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property of the message.</span></span>
  
<span data-ttu-id="8a048-116">Para obter mais informações, consulte [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) seção "pós-transmitir processamento de uma mensagem sinalizado."</span><span class="sxs-lookup"><span data-stu-id="8a048-116">For more information, see [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section "Post-Transmit Processing of a Flagged Message."</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8a048-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a048-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a048-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8a048-118">Protocol specifications</span></span>

<span data-ttu-id="8a048-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a048-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a048-120">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8a048-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8a048-121">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a048-121">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a048-122">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="8a048-122">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="8a048-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a048-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a048-124">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="8a048-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a048-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8a048-125">Header files</span></span>

<span data-ttu-id="8a048-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a048-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a048-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8a048-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a048-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a048-128">Mapitags.h</span></span>
  
> <span data-ttu-id="8a048-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8a048-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a048-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a048-130">See also</span></span>



[<span data-ttu-id="8a048-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8a048-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a048-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8a048-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a048-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8a048-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a048-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8a048-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

