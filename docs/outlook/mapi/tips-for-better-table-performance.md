---
title: Dicas para melhorar o desempenho de tabelas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: da49b4d8251f6b0b69d2ffbf80194943215675e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564161"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="e4bd7-103">Dicas para melhorar o desempenho de tabelas</span><span class="sxs-lookup"><span data-stu-id="e4bd7-103">Tips for better table performance</span></span>
  
<span data-ttu-id="e4bd7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4bd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4bd7-105">Como muitas das operações tabela podem ser demoradas e há um meio para indicar o progresso, é útil usar as seguintes técnicas para melhorar o desempenho:</span><span class="sxs-lookup"><span data-stu-id="e4bd7-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="e4bd7-106">**Tornar [IMAPITable: IUnknown](imapitableiunknown.md) chama na ordem correta**</span><span class="sxs-lookup"><span data-stu-id="e4bd7-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="e4bd7-107">Clientes e provedores de serviços podem trabalhar com tabelas de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="e4bd7-108">Abra a tabela e recuperar os dados de todas as linhas usando o conjunto de coluna padrão e ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="e4bd7-109">Como alternativa, eles podem modificar este modo de exibição padrão da tabela alterando o conjunto de colunas, alterando a ordem de classificação ou estabelecendo uma restrição para restringir o escopo da tabela.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="e4bd7-110">Os usuários da tabela que pretende executar uma ou mais dessas operações antes de recuperar qualquer dado devem realizá-las na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="e4bd7-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="e4bd7-111">Defina uma coluna definidas com [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="e4bd7-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="e4bd7-112">Estabeleça uma restrição com [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="e4bd7-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="e4bd7-113">Defina uma ordem de classificação com [IMAPITable:: SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="e4bd7-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="e4bd7-114">Execução dessas tarefas nesta ordem limita o número de linhas e colunas que serão classificadas, melhorando o desempenho.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="e4bd7-115">**Atraso de uma operação usando o sinalizador TBL_BATCH se possível**</span><span class="sxs-lookup"><span data-stu-id="e4bd7-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="e4bd7-116">A definição de tabela\_sinalizador de LOTE em um método permite que o implementador de tabela coletar várias chamadas antes de agir em qualquer um deles.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="e4bd7-117">Em vez de fazer chamadas potencialmente muitos para um servidor remoto. implementador uma tabela pode tornar um, realizando todas as operações de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="e4bd7-118">Os resultados das operações não são avaliados até que eles sejam necessários.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="e4bd7-119">Por exemplo, quando um cliente chama [IMAPITable:: Restrict](imapitable-restrict.md) para especificar uma restrição com a tabela\_LOTE sinalizador definido, a restrição não precisa entram em vigor até que o cliente chama [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="e4bd7-120">Isso permite que o implementador de tabela combinar o trabalho de duas chamadas para um.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="e4bd7-121">Tabela de usuários que se beneficiam da tabela\_sinalizador de LOTE deve estar ciente de que o tratamento sob estas condições de erro pode ser mais complexo.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="e4bd7-122">Como tratando os erros de uma operação atrasada é semelhante ao tratamento de erros quando MAPI\_DEFERRED_ERRORS sinalizador estiver definido, consulte [Adiar erros de MAPI](deferring-mapi-errors.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="e4bd7-123">**Manter um cache de propriedades comumente usadas**</span><span class="sxs-lookup"><span data-stu-id="e4bd7-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="e4bd7-124">Provedores de serviços de implementação de tabelas podem diminuir o tempo que leva para criar um modo de exibição armazenando em cache cópias das propriedades do objeto comumente usadas.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="e4bd7-125">Manter uma cópia dessas propriedades em gravações de memória precisar recuperá-las a partir do objeto cada vez que o modo de exibição deve ser recriado.</span><span class="sxs-lookup"><span data-stu-id="e4bd7-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4bd7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4bd7-126">See also</span></span>

- [<span data-ttu-id="e4bd7-127">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="e4bd7-127">MAPI Tables</span></span>](mapi-tables.md)

