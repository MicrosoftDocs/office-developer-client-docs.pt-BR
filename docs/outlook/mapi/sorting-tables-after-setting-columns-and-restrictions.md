---
title: Classificando tabelas após definir colunas e restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770480"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="55f49-103">Classificando tabelas após definir colunas e restrições</span><span class="sxs-lookup"><span data-stu-id="55f49-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="55f49-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55f49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55f49-105">Quando você precisa limitar o modo de exibição de uma tabela classificado, sempre verifique as seguintes chamadas **IMAPITable** na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="55f49-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="55f49-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) para definir o conjunto de coluna.</span><span class="sxs-lookup"><span data-stu-id="55f49-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="55f49-107">[IMAPITable:: Restrict](imapitable-restrict.md) para impor a restrição.</span><span class="sxs-lookup"><span data-stu-id="55f49-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="55f49-108">[IMAPITable:: SortTable](imapitable-sorttable.md) para executar a classificação.</span><span class="sxs-lookup"><span data-stu-id="55f49-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="55f49-109">Se a tabela classificada é categorizada, fazer uma chamada para [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), se necessário, após a chamada **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="55f49-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="55f49-110">Essa classificação de chamadas é importante, porque a maioria dos provedores de serviço classificar uma tabela como a última tarefa para obter o melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="55f49-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="55f49-111">Se, por exemplo, um provedor de armazenamento de mensagem deve categorizar a uma tabela de conteúdo de pasta antes de uma restrição pode ser imposta, essa classificação será removida durante o processamento da restrição.</span><span class="sxs-lookup"><span data-stu-id="55f49-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="55f49-112">Uma segunda categorização será necessária.</span><span class="sxs-lookup"><span data-stu-id="55f49-112">A second categorization will be necessary.</span></span> 
  

