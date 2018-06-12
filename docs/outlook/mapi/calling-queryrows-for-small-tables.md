---
title: Chamar QueryRows para tabelas pequenas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 40533470681182719f5009b048e3b173b92ef290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766236"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="5bbf6-103">Chamar QueryRows para tabelas pequenas</span><span class="sxs-lookup"><span data-stu-id="5bbf6-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="5bbf6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bbf6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bbf6-105">Ao recuperar linhas de uma pequena tabela, chame [IMAPITable:: QueryRows](imapitable-queryrows.md) em vez de primeira criando uma restrição.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="5bbf6-106">Criar uma restrição afeta o desempenho, pois o provedor deve primeiro criar uma tabela, encontre as linhas correspondentes na tabela original e copie as linhas para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="5bbf6-107">Se o número total de linhas da tabela for menor do que 100, é provavelmente mais efetiva ler todas as linhas e então chamar [IMAPITable:: FindRow](imapitable-findrow.md) para localizar a linha apropriada.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="5bbf6-108">Essa é uma estratégia de particularmente boa se essa informação é necessária somente ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="5bbf6-109">O tempo adequado para usar uma restrição é quando as informações restritas ou filtradas serão usadas por um período maior de tempo ou usadas frequentemente.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="5bbf6-110">Por exemplo, se você sempre precisa de um modo de exibição com mensagens não lidas, uma restrição é a chamada adequada para usar.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

