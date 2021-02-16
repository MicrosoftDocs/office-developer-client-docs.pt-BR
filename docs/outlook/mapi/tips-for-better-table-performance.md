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
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412510"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="44d19-103">Dicas para melhorar o desempenho de tabelas</span><span class="sxs-lookup"><span data-stu-id="44d19-103">Tips for better table performance</span></span>
  
<span data-ttu-id="44d19-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44d19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44d19-105">Como muitas das operações de tabela podem ser demoradas e não há como indicar o progresso, é útil usar as seguintes técnicas para melhorar o desempenho:</span><span class="sxs-lookup"><span data-stu-id="44d19-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="44d19-106">**Fazer [chamadas IMAPITable : IUnknown](imapitableiunknown.md) na ordem correta**</span><span class="sxs-lookup"><span data-stu-id="44d19-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="44d19-107">Clientes e provedores de serviços podem trabalhar com tabelas de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="44d19-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="44d19-108">Eles podem abrir a tabela e recuperar os dados de todas as linhas usando o conjunto de colunas padrão e a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="44d19-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="44d19-109">Como alternativa, eles podem modificar esse modo de exibição padrão da tabela alterando o conjunto de colunas, alterando a ordem de classificação ou estabelecendo uma restrição para restringir o escopo da tabela.</span><span class="sxs-lookup"><span data-stu-id="44d19-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="44d19-110">Os usuários de tabela que pretendem executar uma ou mais dessas operações antes de recuperar dados devem es performá-los na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="44d19-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="44d19-111">Defina um conjunto de colunas [com IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="44d19-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="44d19-112">Estabeleça uma [restrição com IMAPITable::Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="44d19-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="44d19-113">Defina uma ordem de classificação com [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="44d19-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="44d19-114">A execução dessas tarefas nesta ordem limita o número de linhas e colunas que serão ordenadas, melhorando assim o desempenho.</span><span class="sxs-lookup"><span data-stu-id="44d19-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="44d19-115">**Atrasar uma operação usando o sinalizador de TBL_BATCH, se possível**</span><span class="sxs-lookup"><span data-stu-id="44d19-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="44d19-116">Definir o sinalizador BATCH TBL em um método permite que o implementador de tabela colete várias chamadas antes de \_ agir em qualquer uma delas.</span><span class="sxs-lookup"><span data-stu-id="44d19-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="44d19-117">Em vez de fazer potencialmente muitas chamadas para um servidor remoto; um implementador de tabela pode fazer uma, executando todas as operações de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="44d19-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="44d19-118">Os resultados das operações não são avaliados até que sejam necessários.</span><span class="sxs-lookup"><span data-stu-id="44d19-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="44d19-119">Por exemplo, quando um cliente chama [IMAPITable::Restrict](imapitable-restrict.md) para especificar uma restrição com o sinalizador BATCH TBL definido, a restrição não precisa entrar em vigor até que o cliente chama \_ [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="44d19-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="44d19-120">Isso permite que o implementador de tabela combine o trabalho de duas chamadas em uma.</span><span class="sxs-lookup"><span data-stu-id="44d19-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="44d19-121">Os usuários de tabela que aproveitam o sinalizador batch TBL devem estar cientes de que o tratamento de erros \_ sob essas condições pode ser mais complexo.</span><span class="sxs-lookup"><span data-stu-id="44d19-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="44d19-122">Como a manipulação dos erros de uma operação atrasada é semelhante a lidar com os erros quando o sinalizador mapi DEFERRED_ERRORS está definido, consulte Adiar erros mapi para obter \_ mais informações. [](deferring-mapi-errors.md)</span><span class="sxs-lookup"><span data-stu-id="44d19-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="44d19-123">**Manter um cache de propriedades comumente usadas**</span><span class="sxs-lookup"><span data-stu-id="44d19-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="44d19-124">Os provedores de serviços que implementam tabelas podem diminuir o tempo necessário para criar uma exibição armazenando cópias em cache das propriedades de objeto comumente usadas.</span><span class="sxs-lookup"><span data-stu-id="44d19-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="44d19-125">Manter uma cópia dessas propriedades na memória economiza ter que recuperá-las do objeto sempre que o ponto de vista precisar ser reconstruído.</span><span class="sxs-lookup"><span data-stu-id="44d19-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44d19-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="44d19-126">See also</span></span>

- [<span data-ttu-id="44d19-127">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="44d19-127">MAPI Tables</span></span>](mapi-tables.md)

