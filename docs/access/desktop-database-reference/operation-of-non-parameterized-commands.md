---
title: Operação dos comandos sem parâmetros
TOCTitle: Operation of Non-Parameterized Commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a3e1799e5e40ffa3ffcd6698900b8678b309696e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885154"
---
# <a name="operation-of-non-parameterized-commands"></a><span data-ttu-id="4a543-102">Operação dos comandos sem parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a543-102">Operation of Non-Parameterized Commands</span></span>


<span data-ttu-id="4a543-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a543-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a543-p101">Para os comandos sem parâmetros, todos os comandos do provedor são executados e os **Recordsets** são criados durante a execução do comando. Se o comando for executado de forma síncrona, todos os **Recordsets** serão totalmente preenchidos. Se o modo de preenchimento assíncrono foi selecionado, o estado de preenchimento dos **Recordsets** dependerá do modo de preenchimento e do tamanho dos **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="4a543-p101">For non-parameterized commands, all of the provider commands are executed and the **Recordsets** are created during command execution. If the command is executed synchronously, all of the **Recordsets** will be fully populated. If an asynchronous population mode was selected, the populated state of the **Recordsets** will depend on the population mode and the size of the **Recordsets**.</span></span>

<span data-ttu-id="4a543-107">Por exemplo, o *parent-command* poderia retornar um **conjunto de registros** de clientes para uma empresa de uma tabela de clientes e o *filho-command* poderia retornar um **Recordset** de pedidos para todos os clientes de uma tabela Pedidos.</span><span class="sxs-lookup"><span data-stu-id="4a543-107">For example, the *parent-command* could return a **Recordset** of customers for a company from a Customers table, and the *child-command* could return a **Recordset** of orders for all customers from an Orders table.</span></span>

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

<span data-ttu-id="4a543-108">Para relações pai e filho sem parâmetros, cada objeto **Recordset** pai e filho deve ter uma coluna em comum para associá-los.</span><span class="sxs-lookup"><span data-stu-id="4a543-108">For non-parameterized parent-child relationships, each parent and child **Recordset** object must have a column in common to associate them.</span></span> <span data-ttu-id="4a543-109">As colunas são nomeadas na cláusula RELATE, *coluna pai* primeiro e, em seguida, a *coluna filho*.</span><span class="sxs-lookup"><span data-stu-id="4a543-109">The columns are named in the RELATE clause, *parent-column* first and then *child-column*.</span></span> <span data-ttu-id="4a543-110">As colunas podem ter nomes diferentes nos respectivos objetos **Recordset**, mas devem se referir às mesmas informações para especificar uma relação significativa.</span><span class="sxs-lookup"><span data-stu-id="4a543-110">The columns may have different names in their respective **Recordset** objects but must refer to the same information in order to specify a meaningful relation.</span></span> <span data-ttu-id="4a543-111">Por exemplo, os objetos **Customers** e **Orders** e **Recordset** não poderiam ter ambos um campo customerID.</span><span class="sxs-lookup"><span data-stu-id="4a543-111">For example, the **Customers** and **Orders** **Recordset** objects could both have a customerID field.</span></span> <span data-ttu-id="4a543-112">Como a associação do **Recordset** filho é determinada pelo comando do provedor, é possível que esse **Recordset** tenha linhas órfãs.</span><span class="sxs-lookup"><span data-stu-id="4a543-112">Because the membership of the child **Recordset** is determined by the provider command, it is possible for the child **Recordset** to contain orphaned rows.</span></span> <span data-ttu-id="4a543-113">Essas linhas são inacessíveis sem a alteração posterior da forma.</span><span class="sxs-lookup"><span data-stu-id="4a543-113">These orphaned rows are inaccessible without further reshaping.</span></span>

<span data-ttu-id="4a543-114">Data shaping acrescenta uma coluna de capítulo ao **Recordset**pai.</span><span class="sxs-lookup"><span data-stu-id="4a543-114">Data shaping appends a chapter column to the parent **Recordset**.</span></span> <span data-ttu-id="4a543-115">Os valores na coluna de capítulo são referências às linhas do **Recordset**, filho que satisfazem cláusula RELATE.</span><span class="sxs-lookup"><span data-stu-id="4a543-115">The values in the chapter column are references to rows in the child **Recordset**, which satisfy the RELATE clause.</span></span> <span data-ttu-id="4a543-116">Ou seja, o mesmo valor é na *coluna pai* de uma linha pai determinado como está na *coluna filha* de todas as linhas do filho capítulo.</span><span class="sxs-lookup"><span data-stu-id="4a543-116">That is, the same value is in the *parent-column* of a given parent row as is in the *child-column* of all the rows of the chapter child.</span></span> <span data-ttu-id="4a543-117">Quando várias cláusulas para são usadas na mesma cláusula RELATE, eles são combinados implicitamente usando um operador AND.</span><span class="sxs-lookup"><span data-stu-id="4a543-117">When multiple TO clauses are used in the same RELATE clause, they are implicitly combined using an AND operator.</span></span> <span data-ttu-id="4a543-118">Se as colunas pai na cláusula relate não constituem uma chave ao **Recordset**pai, uma linha única filho pode ter várias linhas pai.</span><span class="sxs-lookup"><span data-stu-id="4a543-118">If the parent columns in the relate clause do not constitute a key to the parent **Recordset**, a single child row may have multiple parent rows.</span></span>

<span data-ttu-id="4a543-p104">Quando você acessa a referência na coluna de capítulo, o ADO recupera automaticamente o **Recordset** representado pela referência. Observe que em um comando sem parâmetros, ainda que o **Recordset** filho inteiro possa ser recuperado, o capítulo apresentará somente um subconjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="4a543-p104">When you access the reference in the chapter column, ADO automatically retrieves the **Recordset** represented by the reference. Note that in a non-parameterized command, although the entire child **Recordset** has been retrieved, the chapter only presents a subset of rows.</span></span>

<span data-ttu-id="4a543-p105">Se a coluna acrescentada não tiver um *alias de capítulo*, será gerado um nome para ela automaticamente. Um objeto [Field](field-object-ado.md) para a coluna será acrescentado à coleção [Fields](fields-collection-ado.md) do objeto **Recordset** e esse tipo de dados será **adChapter**.</span><span class="sxs-lookup"><span data-stu-id="4a543-p105">If the appended column has no *chapter-alias*, a name will be generated for it automatically. A [Field](field-object-ado.md) object for the column will be appended to the **Recordset** object's [Fields](fields-collection-ado.md) collection, and its data type will be **adChapter**.</span></span>

<span data-ttu-id="4a543-123">Para obter informações sobre como navegar em um **Recordset** hierárquico, consulte [Acessando linhas em um conjunto de registros hierárquico](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="4a543-123">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

