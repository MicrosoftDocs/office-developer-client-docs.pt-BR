---
title: Chamar QueryRows para tabelas pequenas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331622"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="46be0-103">Chamar QueryRows para tabelas pequenas</span><span class="sxs-lookup"><span data-stu-id="46be0-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="46be0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46be0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46be0-105">Ao recuperar linhas de uma tabela pequena, chame imApitable [:: QueryRows](imapitable-queryrows.md) em vez de primeiro criar uma restrição.</span><span class="sxs-lookup"><span data-stu-id="46be0-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="46be0-106">A criação de uma restrição impacta o desempenho porque o provedor deve primeiro criar uma tabela, localizar as linhas correspondentes na tabela original e, em seguida, copiar as linhas para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="46be0-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="46be0-107">Se o número total de linhas na tabela for menor que 100, provavelmente será mais eficaz ler todas as linhas e, em seguida, chamar imApitable [:: FindRow](imapitable-findrow.md) para localizar a linha apropriada.</span><span class="sxs-lookup"><span data-stu-id="46be0-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="46be0-108">Essa é uma estratégia particularmente boa se essas informações são necessárias apenas ocasionalmente.</span><span class="sxs-lookup"><span data-stu-id="46be0-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="46be0-109">O momento apropriado para usar uma restrição é quando as informações restritas ou filtradas serão usadas por um período de tempo maior ou quando usadas com frequência.</span><span class="sxs-lookup"><span data-stu-id="46be0-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="46be0-110">Por exemplo, se você sempre precisa de um modo de exibição com mensagens não lidas, uma restrição é a chamada adequada a ser usada.</span><span class="sxs-lookup"><span data-stu-id="46be0-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

