---
title: Classificação e categorização
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Modificado pela última vez: 08 de novembro de 2011'
ms.openlocfilehash: 12668cb87f21b56cd398a7b5375f6a4b40c65829
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581528"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="dd357-103">Classificação e categorização</span><span class="sxs-lookup"><span data-stu-id="dd357-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="dd357-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd357-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd357-105">Classificar uma tabela coloca as linhas em uma ordem que faz sentido para seu visualizador.</span><span class="sxs-lookup"><span data-stu-id="dd357-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="dd357-106">Por exemplo, um visualizador pode preferir ver o índice de conteúdo de uma pasta classificada por assunto da mensagem, para que todos os threads de uma conversa sejam juntos enquanto outro visualizador pode querer as mensagens classificadas pelo nome do remetente.</span><span class="sxs-lookup"><span data-stu-id="dd357-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="dd357-107">Uma tabela instâncias recém-criadas não é necessariamente classificada em alguma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="dd357-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="dd357-108">Existem dois tipos de classificação:</span><span class="sxs-lookup"><span data-stu-id="dd357-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="dd357-109">Classificação padrão</span><span class="sxs-lookup"><span data-stu-id="dd357-109">Standard sorting</span></span>
    
- <span data-ttu-id="dd357-110">Categorizados classificação</span><span class="sxs-lookup"><span data-stu-id="dd357-110">Categorized sorting</span></span> 
    
<span data-ttu-id="dd357-111">Com a classificação padrão, todas as linhas são exibidas em uma lista plana usando uma ou mais colunas como uma chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="dd357-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="dd357-112">Com a classificação categorizada, as linhas são exibidas hierarquicamente com uma ou mais colunas como a chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="dd357-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="dd357-113">Em cada categoria, há uma linha de título especial que contém as seguintes colunas.</span><span class="sxs-lookup"><span data-stu-id="dd357-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="dd357-114">A coluna ou colunas que compõem a chave de classificação</span><span class="sxs-lookup"><span data-stu-id="dd357-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="dd357-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dd357-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="dd357-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dd357-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="dd357-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dd357-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="dd357-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dd357-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="dd357-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dd357-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="dd357-120">Recuados sob a linha do cabeçalho são todas as linhas da tabela que contêm colunas com valores que correspondem a chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="dd357-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="dd357-121">Essas linhas são chamadas as linhas da folha.</span><span class="sxs-lookup"><span data-stu-id="dd357-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="dd357-122">Linhas de folha contêm todas as colunas na coluna definir menos as colunas de chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="dd357-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="dd357-123">Geralmente, os índices de conteúdo de pastas suportam a classificação categorizada além de classificar standard.</span><span class="sxs-lookup"><span data-stu-id="dd357-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="dd357-124">Normalmente, os índices de conteúdo de contêineres do catálogo de endereços suportam a classificação apenas standard.</span><span class="sxs-lookup"><span data-stu-id="dd357-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="dd357-125">Uma categoria pode ter dois estados: expandida e recolhida.</span><span class="sxs-lookup"><span data-stu-id="dd357-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="dd357-126">Quando uma categoria está no estado recolhido, somente a linha do cabeçalho é retornada da [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="dd357-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="dd357-127">Quando uma categoria está no estado expandido, todas as linhas relacionadas à categoria são retornadas.</span><span class="sxs-lookup"><span data-stu-id="dd357-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="dd357-128">Isso inclui a linha do cabeçalho e as linhas da folha.</span><span class="sxs-lookup"><span data-stu-id="dd357-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="dd357-129">Cada categoria em um modo de exibição de tabela pode ser expandida ou recolhida de forma independente.</span><span class="sxs-lookup"><span data-stu-id="dd357-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="dd357-130">Ou seja, não todas as categorias devem estar no mesmo estado ao mesmo tempo; Algumas categorias podem ser recolhidas, enquanto outras são expandidas.</span><span class="sxs-lookup"><span data-stu-id="dd357-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="dd357-131">O usuário de uma tabela categorizado decidirá como ele é exibido.</span><span class="sxs-lookup"><span data-stu-id="dd357-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="dd357-132">Uma opção comum é usar um controle fornecido no SDK do Windows chamado controle treeview.</span><span class="sxs-lookup"><span data-stu-id="dd357-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="dd357-133">Controles TreeView são caixas de listagem informações de suporte em uma estrutura de árvore.</span><span class="sxs-lookup"><span data-stu-id="dd357-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="dd357-134">Linhas de título para categorias no estado expandido estão marcadas com um sinal de menos enquanto linhas do título para categorias no estado recolhido são marcadas com um sinal de adição.</span><span class="sxs-lookup"><span data-stu-id="dd357-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="dd357-135">Expandida categorias são exibidas com as linhas da folha recuadas sob as linhas de título.</span><span class="sxs-lookup"><span data-stu-id="dd357-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="dd357-136">Para recolher e expandir uma categoria, um provedor de serviço ou um aplicativo cliente usa os seguintes [IMAPITable: IUnknown](imapitableiunknown.md) métodos:</span><span class="sxs-lookup"><span data-stu-id="dd357-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="dd357-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="dd357-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="dd357-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="dd357-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="dd357-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="dd357-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="dd357-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="dd357-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="dd357-141">Para obter mais informações sobre como classificar os threads de uma conversa consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="dd357-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="dd357-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="dd357-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="dd357-143">Propriedade canônica PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="dd357-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="dd357-144">Propriedade canônica PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="dd357-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="dd357-145">Propriedade canônica PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="dd357-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="dd357-146">Propriedade canônica PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="dd357-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="dd357-147">Propriedade canônica PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="dd357-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="dd357-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="dd357-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="dd357-149">Classificar tabelas depois de configurar colunas e restrições</span><span class="sxs-lookup"><span data-stu-id="dd357-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="dd357-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd357-150">See also</span></span>



[<span data-ttu-id="dd357-151">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="dd357-151">MAPI Tables</span></span>](mapi-tables.md)

