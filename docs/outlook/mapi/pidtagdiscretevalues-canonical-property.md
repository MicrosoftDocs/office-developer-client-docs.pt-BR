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
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404838"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="9b4fc-103">Propriedade canônica PidTagDiscreteValues</span><span class="sxs-lookup"><span data-stu-id="9b4fc-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="9b4fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b4fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b4fc-105">Contém TRUE se um relatório de não entrega só se aplica a membros discretos de uma lista de distribuição, e não à lista inteira.</span><span class="sxs-lookup"><span data-stu-id="9b4fc-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b4fc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9b4fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b4fc-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="9b4fc-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="9b4fc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9b4fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b4fc-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="9b4fc-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="9b4fc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9b4fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b4fc-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9b4fc-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9b4fc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9b4fc-112">Area:</span></span>  <br/> |<span data-ttu-id="9b4fc-113">MAPI não-transmittable</span><span class="sxs-lookup"><span data-stu-id="9b4fc-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b4fc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b4fc-114">Remarks</span></span>

<span data-ttu-id="9b4fc-115">Essa propriedade é usada em um relatório de não entrega quando a mensagem não pôde ser entregue a um ou mais membros de uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="9b4fc-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="9b4fc-116">Sua finalidade é limitar as tentativas de retransmissão a apenas os membros individuais e não à lista de distribuição como um todo.</span><span class="sxs-lookup"><span data-stu-id="9b4fc-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="9b4fc-117">A tabela de destinatários de um relatório de não entrega contém entradas para todos os destinatários aos quais a mensagem não pôde ser entregue e também para as listas de distribuição, se houver, às quais pertencem.</span><span class="sxs-lookup"><span data-stu-id="9b4fc-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="9b4fc-118">O provedor de transporte deve definir essa propriedade como TRUE para cada entrada de lista de distribuição e deve copiar o **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) da lista de distribuição para o **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) e **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) para cada membro dessa lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="9b4fc-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="9b4fc-119">**PR_DISCRETE_VALUES** não deve ser definido para qualquer entrada de destinatário de relatório de não entrega que não seja uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="9b4fc-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9b4fc-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b4fc-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9b4fc-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9b4fc-121">Header files</span></span>

<span data-ttu-id="9b4fc-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9b4fc-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b4fc-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9b4fc-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b4fc-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9b4fc-124">Mapitags.h</span></span>
  
> <span data-ttu-id="9b4fc-125">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="9b4fc-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b4fc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b4fc-126">See also</span></span>



[<span data-ttu-id="9b4fc-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9b4fc-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b4fc-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9b4fc-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b4fc-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9b4fc-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b4fc-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9b4fc-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

