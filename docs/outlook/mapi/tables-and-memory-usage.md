---
title: Tabelas e uso de memória
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 383c03a00509447222204ab729c56f5eeac553df
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563013"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="74601-103">Tabelas e uso de memória</span><span class="sxs-lookup"><span data-stu-id="74601-103">Tables and memory usage</span></span>

<span data-ttu-id="74601-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74601-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74601-105">Uma questão importante conectada com a recuperação de dados de uma tabela é o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="74601-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="74601-106">Falta de memória disponível pode causar [IMAPITable:: QueryRows](imapitable-queryrows.md) e [HrQueryAllRows](hrqueryallrows.md) falha, retornando menor do que o número de linhas desejado.</span><span class="sxs-lookup"><span data-stu-id="74601-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="74601-107">Decidir qual método ou a função a ser usada para recuperar dados da tabela depende se a tabela pode ser esperada para ajustá-la na memória e se for possível, se a falha é aceitável.</span><span class="sxs-lookup"><span data-stu-id="74601-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="74601-108">Porque nem sempre é fácil determinar a quantidade de dados que se ajustarão à memória ao mesmo tempo, MAPI fornece algumas diretrizes básicas para um aplicativo cliente ou o provedor de serviço a seguir.</span><span class="sxs-lookup"><span data-stu-id="74601-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="74601-109">Lembre-se de que sempre há exceções, com base em como os dados subjacentes são armazenados e a implementação de determinada tabela.</span><span class="sxs-lookup"><span data-stu-id="74601-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="74601-110">As diretrizes a seguir podem ser usadas para avaliar o uso de memória da tabela:</span><span class="sxs-lookup"><span data-stu-id="74601-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="74601-111">Os clientes que podem tolerar ocasionais uso de memória de conjunto de trabalho no intervalo megabyte e podem assumir que eles têm problemas de leitura de uma tabela inteira na memória.</span><span class="sxs-lookup"><span data-stu-id="74601-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="74601-112">Restrições tem um efeito sobre o uso de uma tabela de memória.</span><span class="sxs-lookup"><span data-stu-id="74601-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="74601-113">Para ajustá-la na memória enquanto uma tabela grande unrestricted geralmente não pode, espera-se uma tabela está seriamente restrita com um amplo número de linhas, como uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="74601-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="74601-114">Várias tabelas do pertencentes a MAPI, como status, perfil, o serviço de mensagem, provedor e tabelas de repositório de mensagens, geralmente couberem na memória.</span><span class="sxs-lookup"><span data-stu-id="74601-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="74601-115">Estas são as tabelas geralmente é pequenas.</span><span class="sxs-lookup"><span data-stu-id="74601-115">These are generally small tables.</span></span> <span data-ttu-id="74601-116">No entanto, há exceções.</span><span class="sxs-lookup"><span data-stu-id="74601-116">However, there are exceptions.</span></span> <span data-ttu-id="74601-117">Por exemplo, um provedor de perfil baseado em servidor pode gerar uma tabela maior de perfil que não será possível para ajustá-la.</span><span class="sxs-lookup"><span data-stu-id="74601-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="74601-118">Para recuperar todas as linhas de uma tabela que se ajustarão à memória sem problemas, chame [HrQueryAllRows](hrqueryallrows.md), definindo o número máximo de linhas a zero.</span><span class="sxs-lookup"><span data-stu-id="74601-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="74601-119">Para recuperar todas as linhas de uma tabela que pode ou não pode cabem na memória, gerar um erro, chame **HrQueryAllRows** especificando um número máximo de linhas.</span><span class="sxs-lookup"><span data-stu-id="74601-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="74601-120">O número máximo de linhas deve ser definido para um número maior que o número mínimo de linhas que são necessários.</span><span class="sxs-lookup"><span data-stu-id="74601-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="74601-121">Se um cliente deve acessar pelo menos 50 linhas de uma tabela de 300 linha, o número máximo de linhas deve ser definido como 51 pelo menos.</span><span class="sxs-lookup"><span data-stu-id="74601-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="74601-122">Para recuperar todas as linhas de uma tabela que não é esperada para ajustá-la na memória, chame [IMAPITable:: QueryRows](imapitable-queryrows.md) em um loop com uma contagem de linha relativamente pequeno, como mostra o exemplo de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="74601-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

<span data-ttu-id="74601-123">Quando este loop for concluído e todas as linhas na tabela foram processadas e _pássaros_ é zero, geralmente será a posição do cursor na parte inferior da tabela.</span><span class="sxs-lookup"><span data-stu-id="74601-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74601-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="74601-124">See also</span></span>

- [<span data-ttu-id="74601-125">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="74601-125">MAPI Tables</span></span>](mapi-tables.md)

