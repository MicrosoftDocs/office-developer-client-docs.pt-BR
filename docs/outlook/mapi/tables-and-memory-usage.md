---
title: Tabelas e o uso da memória
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436857"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="ead62-103">Tabelas e o uso da memória</span><span class="sxs-lookup"><span data-stu-id="ead62-103">Tables and memory usage</span></span>

<span data-ttu-id="ead62-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ead62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ead62-105">Um problema importante conectado à recuperação de dados de uma tabela é o uso da memória.</span><span class="sxs-lookup"><span data-stu-id="ead62-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="ead62-106">A falta de memória disponível pode causar falha em [IMAPITable::QueryRows](imapitable-queryrows.md) e [HrQueryAllRows,](hrqueryallrows.md) retornando menos do que o número desejado de linhas.</span><span class="sxs-lookup"><span data-stu-id="ead62-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="ead62-107">Decidir qual método ou função usar para recuperar dados de tabela depende se a tabela deve caber na memória e, se não puder, se a falha for aceitável.</span><span class="sxs-lookup"><span data-stu-id="ead62-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="ead62-108">Como nem sempre é fácil determinar a quantidade de dados que caberá na memória de uma só vez, o MAPI fornece algumas diretrizes básicas para que um provedor de serviços ou aplicativo cliente siga.</span><span class="sxs-lookup"><span data-stu-id="ead62-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="ead62-109">Lembre-se de que sempre há exceções, com base na implementação de tabela específica e em como os dados subjacentes são armazenados.</span><span class="sxs-lookup"><span data-stu-id="ead62-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="ead62-110">As diretrizes a seguir podem ser usadas para avaliar o uso da memória da tabela:</span><span class="sxs-lookup"><span data-stu-id="ead62-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="ead62-111">Clientes que podem tolerar o uso ocasional de memória do conjunto de trabalho no intervalo de megabyte e podem supor que não terão problemas ao ler uma tabela inteira na memória.</span><span class="sxs-lookup"><span data-stu-id="ead62-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="ead62-112">As restrições afetam o uso de memória de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="ead62-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="ead62-113">Uma tabela gravemente restrita com um grande número de linhas, como uma tabela de conteúdo, pode ser esperada para caber na memória enquanto uma tabela grande irrestrita normalmente não pode.</span><span class="sxs-lookup"><span data-stu-id="ead62-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="ead62-114">Várias das tabelas pertencentes a MAPI, como status, perfil, serviço de mensagens, provedor e tabelas de armazenamento de mensagens, geralmente caberão na memória.</span><span class="sxs-lookup"><span data-stu-id="ead62-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="ead62-115">Geralmente, são tabelas pequenas.</span><span class="sxs-lookup"><span data-stu-id="ead62-115">These are generally small tables.</span></span> <span data-ttu-id="ead62-116">No entanto, há exceções.</span><span class="sxs-lookup"><span data-stu-id="ead62-116">However, there are exceptions.</span></span> <span data-ttu-id="ead62-117">Por exemplo, um provedor de perfil baseado em servidor pode gerar uma tabela de perfil maior que não será capaz de caber.</span><span class="sxs-lookup"><span data-stu-id="ead62-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="ead62-118">Para recuperar todas as linhas de uma tabela que caberá na memória sem problemas, chame [HrQueryAllRows](hrqueryallrows.md), definindo o número máximo de linhas como zero.</span><span class="sxs-lookup"><span data-stu-id="ead62-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="ead62-119">Para recuperar todas as linhas de uma tabela que pode ou não caber na memória, gerando um erro, chame **HrQueryAllRows** especificando um número máximo de linhas.</span><span class="sxs-lookup"><span data-stu-id="ead62-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="ead62-120">O número máximo de linhas deve ser definido como um número maior do que o número mínimo de linhas necessárias.</span><span class="sxs-lookup"><span data-stu-id="ead62-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="ead62-121">Se um cliente tiver que acessar pelo menos 50 linhas de uma tabela de 300 linhas, o número máximo de linhas deverá ser definido como pelo menos 51.</span><span class="sxs-lookup"><span data-stu-id="ead62-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="ead62-122">Para recuperar todas as linhas de uma tabela que não deve caber na memória, chame [IMAPITable::QueryRows](imapitable-queryrows.md) em um loop com uma contagem de linhas relativamente pequena, como ilustra o exemplo de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="ead62-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="ead62-123">Quando esse loop for concluído e todas as linhas da tabela foram processadas e  _cRows_ for zero, a posição do cursor normalmente estará na parte inferior da tabela.</span><span class="sxs-lookup"><span data-stu-id="ead62-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ead62-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ead62-124">See also</span></span>

- [<span data-ttu-id="ead62-125">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="ead62-125">MAPI Tables</span></span>](mapi-tables.md)

