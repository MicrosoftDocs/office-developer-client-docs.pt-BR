---
title: Classificar tabelas após definir colunas e restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409878"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="f5f34-103">Classificar tabelas após definir colunas e restrições</span><span class="sxs-lookup"><span data-stu-id="f5f34-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="f5f34-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5f34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5f34-105">Quando você precisar limitar o modo de exibição de uma tabela ordenada, sempre faça as seguintes chamadas **IMAPITable** na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="f5f34-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="f5f34-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) para definir o conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="f5f34-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="f5f34-107">[IMAPITable::Restrict](imapitable-restrict.md) para impor a restrição.</span><span class="sxs-lookup"><span data-stu-id="f5f34-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="f5f34-108">[IMAPITable::SortTable](imapitable-sorttable.md) para executar a classificação.</span><span class="sxs-lookup"><span data-stu-id="f5f34-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="f5f34-109">Se a tabela classificada for categorizada, faça uma chamada para [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), se necessário, após a **chamada sorttable.**</span><span class="sxs-lookup"><span data-stu-id="f5f34-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="f5f34-110">Essa ordem de chamadas é importante porque a maioria dos provedores de serviços classificar uma tabela como a última tarefa para obter o melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="f5f34-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="f5f34-111">Se, por exemplo, um provedor de armazenamento de mensagens tiver que categorizar uma tabela de conteúdo de pasta antes que uma restrição possa ser imposta, essa categorização será removida durante o processamento da restrição.</span><span class="sxs-lookup"><span data-stu-id="f5f34-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="f5f34-112">Uma segunda categorização será necessária.</span><span class="sxs-lookup"><span data-stu-id="f5f34-112">A second categorization will be necessary.</span></span> 
  

