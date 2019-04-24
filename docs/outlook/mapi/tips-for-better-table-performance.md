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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327794"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="584dc-103">Dicas para melhorar o desempenho de tabelas</span><span class="sxs-lookup"><span data-stu-id="584dc-103">Tips for better table performance</span></span>
  
<span data-ttu-id="584dc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="584dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="584dc-105">Como muitas das operações de tabela podem ser demoradas e não há como indicar o progresso, é útil usar as seguintes técnicas para melhorar o desempenho:</span><span class="sxs-lookup"><span data-stu-id="584dc-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="584dc-106">**Tornar [IMAPITable:](imapitableiunknown.md) as chamadas IUnknown na ordem correta**</span><span class="sxs-lookup"><span data-stu-id="584dc-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="584dc-107">Os clientes e provedores de serviços podem trabalhar com tabelas de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="584dc-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="584dc-108">Eles podem abrir a tabela e recuperar os dados de todas as linhas usando o conjunto de colunas padrão e a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="584dc-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="584dc-109">Como alternativa, eles podem modificar esse modo de exibição padrão da tabela alterando o conjunto de colunas, alterando a ordem de classificação ou estabelecendo uma restrição para restringir o escopo da tabela.</span><span class="sxs-lookup"><span data-stu-id="584dc-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="584dc-110">Os usuários de tabela que pretendem executar uma ou mais dessas operações antes de recuperar quaisquer dados devem executá-los na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="584dc-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="584dc-111">Defina um conjunto de colunas com imApitable [::](imapitable-setcolumns.md)SetColumns.</span><span class="sxs-lookup"><span data-stu-id="584dc-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="584dc-112">Estabeleça uma restrição com [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="584dc-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="584dc-113">Definir uma ordem de classificação com imApitable [:: SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="584dc-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="584dc-114">A execução dessas tarefas nesta ordem limita o número de linhas e colunas que serão classificadas, melhorando assim o desempenho.</span><span class="sxs-lookup"><span data-stu-id="584dc-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="584dc-115">**Retardar uma operação usando o sinalizador TBL_BATCH, se possível**</span><span class="sxs-lookup"><span data-stu-id="584dc-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="584dc-116">Definir o sinalizador\_de lote tbl em um método permite que o implementador de tabelas colete várias chamadas antes de agir em qualquer uma delas.</span><span class="sxs-lookup"><span data-stu-id="584dc-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="584dc-117">Em vez de fazer muitas chamadas para um servidor remoto; um implementador de tabela pode fazer um, realizando todas as operações de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="584dc-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="584dc-118">Os resultados das operações não são avaliados até que sejam necessários.</span><span class="sxs-lookup"><span data-stu-id="584dc-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="584dc-119">Por exemplo, quando um cliente chama [IMAPITable:: Restrict](imapitable-restrict.md) para especificar uma restrição\_com o sinalizador de lote tbl definido, a restrição não precisa entrar em vigor até que o cliente chame IMAPITable [:: QueryRows](imapitable-queryrows.md) para recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="584dc-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="584dc-120">Isso permite que o implementador de tabela Combine o trabalho de duas chamadas em uma.</span><span class="sxs-lookup"><span data-stu-id="584dc-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="584dc-121">Os usuários de tabela que aproveitam o\_sinalizador de lote tbl devem estar cientes de que o tratamento de erros nessas condições pode ser mais complexo.</span><span class="sxs-lookup"><span data-stu-id="584dc-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="584dc-122">Como manipular os erros de uma operação atrasada é semelhante a lidar com os erros quando o\_sinalizador MAPI DEFERRED_ERRORS é definido, confira a [referência de erros MAPI](deferring-mapi-errors.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="584dc-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="584dc-123">**Manter um cache de propriedades comumente usadas**</span><span class="sxs-lookup"><span data-stu-id="584dc-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="584dc-124">Os provedores de serviços que implementam tabelas podem reduzir o tempo de criação de um modo de exibição por meio de cache de cópias de propriedades de objeto comumente usadas.</span><span class="sxs-lookup"><span data-stu-id="584dc-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="584dc-125">Manter uma cópia dessas propriedades na memória salva ter que recuperá-las do objeto cada vez que o modo de exibição deve ser recriado.</span><span class="sxs-lookup"><span data-stu-id="584dc-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="584dc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="584dc-126">See also</span></span>

- [<span data-ttu-id="584dc-127">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="584dc-127">MAPI Tables</span></span>](mapi-tables.md)

