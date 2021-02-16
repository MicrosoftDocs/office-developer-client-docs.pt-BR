---
title: Classificação e categorização
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418481"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="97617-103">Classificação e categorização</span><span class="sxs-lookup"><span data-stu-id="97617-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="97617-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97617-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97617-105">Classificar uma tabela coloca linhas em uma ordem que faz sentido para seu visualizador.</span><span class="sxs-lookup"><span data-stu-id="97617-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="97617-106">Por exemplo, um visualizador pode preferir ver o índice de conteúdo de uma pasta classificar por assunto da mensagem para que todos os threads de uma conversa ficam juntos enquanto outro visualizador pode querer que as mensagens sejam ordenadas pelo nome do remetente.</span><span class="sxs-lookup"><span data-stu-id="97617-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="97617-107">Uma tabela recém-criada não é necessariamente ordenada em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="97617-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="97617-108">Há dois tipos de classificação:</span><span class="sxs-lookup"><span data-stu-id="97617-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="97617-109">Classificação padrão</span><span class="sxs-lookup"><span data-stu-id="97617-109">Standard sorting</span></span>
    
- <span data-ttu-id="97617-110">Classificação categorizada</span><span class="sxs-lookup"><span data-stu-id="97617-110">Categorized sorting</span></span> 
    
<span data-ttu-id="97617-111">Com a classificação padrão, todas as linhas são exibidas em uma lista simples usando uma ou mais colunas como uma chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="97617-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="97617-112">Com a classificação categorizada, as linhas são exibidas hierarquicamente com uma ou mais colunas como a chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="97617-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="97617-113">Em cada categoria, há uma linha de título especial que contém as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="97617-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="97617-114">A coluna ou colunas que com a chave de classificação</span><span class="sxs-lookup"><span data-stu-id="97617-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="97617-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="97617-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="97617-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="97617-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="97617-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="97617-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="97617-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="97617-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="97617-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="97617-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="97617-120">Recuados sob a linha de título são todas as linhas da tabela que contêm colunas com valores que corresponderem à chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="97617-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="97617-121">Essas linhas são chamadas de linhas folha.</span><span class="sxs-lookup"><span data-stu-id="97617-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="97617-122">As linhas Leaf contêm todas as colunas no conjunto de colunas menos as colunas de chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="97617-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="97617-123">Os índices de conteúdo de pastas geralmente suportam a classificação categorizada, além da classificação padrão.</span><span class="sxs-lookup"><span data-stu-id="97617-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="97617-124">Os índices de conteúdo dos contêineres do livro de endereços normalmente suportam apenas a classificação padrão.</span><span class="sxs-lookup"><span data-stu-id="97617-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="97617-125">Uma categoria pode ter dois estados: recolhido e expandido.</span><span class="sxs-lookup"><span data-stu-id="97617-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="97617-126">Quando uma categoria está no estado recolhido, somente a linha de título é retornada de [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="97617-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="97617-127">Quando uma categoria está no estado expandido, todas as linhas relacionadas à categoria são retornadas.</span><span class="sxs-lookup"><span data-stu-id="97617-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="97617-128">Isso inclui a linha de título e as linhas folha.</span><span class="sxs-lookup"><span data-stu-id="97617-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="97617-129">Cada categoria em um exibição de tabela pode ser expandida ou recolhido independentemente.</span><span class="sxs-lookup"><span data-stu-id="97617-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="97617-130">Ou seja, nem todas as categorias devem estar no mesmo estado ao mesmo tempo; algumas categorias podem ser recolhidos enquanto outras são expandidas.</span><span class="sxs-lookup"><span data-stu-id="97617-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="97617-131">O usuário de uma tabela categorizada decide como ela é exibida.</span><span class="sxs-lookup"><span data-stu-id="97617-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="97617-132">Uma opção comum é usar um controle fornecido no SDK do Windows chamado controle treeview.</span><span class="sxs-lookup"><span data-stu-id="97617-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="97617-133">Controles treeview são caixas de listagem que suportam informações em uma estrutura em forma de árvore.</span><span class="sxs-lookup"><span data-stu-id="97617-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="97617-134">As linhas de título para categorias no estado expandido são marcadas com um sinal de menos enquanto as linhas de título para categorias no estado recolhido são marcadas com um sinal de mais.</span><span class="sxs-lookup"><span data-stu-id="97617-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="97617-135">As categorias expandidas são exibidas com as linhas folha recuadas sob as linhas de título.</span><span class="sxs-lookup"><span data-stu-id="97617-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="97617-136">Para collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span><span class="sxs-lookup"><span data-stu-id="97617-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="97617-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="97617-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="97617-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="97617-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="97617-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="97617-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="97617-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="97617-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="97617-141">Para obter mais informações sobre como classificar os threads de uma conversa, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="97617-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="97617-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="97617-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="97617-143">Propriedade canônica PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="97617-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="97617-144">Propriedade canônica PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="97617-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="97617-145">Propriedade canônica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="97617-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="97617-146">Propriedade canônica PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="97617-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="97617-147">Propriedade canônica PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="97617-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="97617-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="97617-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="97617-149">Classificar tabelas após definir colunas e restrições</span><span class="sxs-lookup"><span data-stu-id="97617-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="97617-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="97617-150">See also</span></span>



[<span data-ttu-id="97617-151">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="97617-151">MAPI Tables</span></span>](mapi-tables.md)

