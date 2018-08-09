---
title: Propriedade canônica PidTagDiscreteValues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9911d6cee40637a69dfaf432be0e6d42bf38bccd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769200"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="e6eb5-103">Propriedade canônica PidTagDiscreteValues</span><span class="sxs-lookup"><span data-stu-id="e6eb5-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="e6eb5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6eb5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6eb5-105">Conterá TRUE se um relatório de não entrega aplica discretos apenas como membros de uma lista de distribuição em vez de toda a lista.</span><span class="sxs-lookup"><span data-stu-id="e6eb5-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6eb5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e6eb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6eb5-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="e6eb5-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="e6eb5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e6eb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e6eb5-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="e6eb5-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="e6eb5-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e6eb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="e6eb5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e6eb5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e6eb5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e6eb5-112">Area:</span></span>  <br/> |<span data-ttu-id="e6eb5-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="e6eb5-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6eb5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6eb5-114">Remarks</span></span>

<span data-ttu-id="e6eb5-115">Essa propriedade é usada dentro de um relatório de não entrega quando a mensagem não pôde ser entregue a um ou mais membros de uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e6eb5-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="e6eb5-116">Seu objetivo é limitar a retransmissão tenta somente aqueles membros individuais e não a lista de distribuição como um todo.</span><span class="sxs-lookup"><span data-stu-id="e6eb5-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="e6eb5-117">A tabela de destinatários de um relatório de não entrega contém entradas para todos os destinatários para quem a mensagem não pôde ser entregue e também para as listas de distribuição, se houver, às quais eles pertencem.</span><span class="sxs-lookup"><span data-stu-id="e6eb5-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="e6eb5-118">O provedor de transporte deve definir esta propriedade como TRUE para cada entrada da lista de distribuição, e ele deve copiar o **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) da lista de distribuição **PR_ORIGINAL_SEARCH_KEY** ([ , **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) e **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)) PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) propriedades para cada membro dessa lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e6eb5-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="e6eb5-119">**PR_DISCRETE_VALUES** não devem ser definidas para qualquer entrada de destinatários de relatório de não entrega que não seja uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e6eb5-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e6eb5-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6eb5-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e6eb5-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e6eb5-121">Header files</span></span>

<span data-ttu-id="e6eb5-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6eb5-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6eb5-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e6eb5-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="e6eb5-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e6eb5-124">Mapitags.h</span></span>
  
> <span data-ttu-id="e6eb5-125">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="e6eb5-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6eb5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6eb5-126">See also</span></span>



[<span data-ttu-id="e6eb5-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e6eb5-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6eb5-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e6eb5-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6eb5-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e6eb5-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6eb5-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e6eb5-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

