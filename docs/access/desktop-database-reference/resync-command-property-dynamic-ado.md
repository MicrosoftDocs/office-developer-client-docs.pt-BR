---
title: Propriedade Resync Command -- Dinâmica (ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fc64a51044f219d4daae44a9c684506cd7bd5c6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462888"
---
# <a name="resync-command-property--dynamic-ado"></a><span data-ttu-id="ea549-102">Propriedade Resync Command -- Dinâmica (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea549-102">Resync Command Property--Dynamic (ADO)</span></span>

<span data-ttu-id="ea549-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea549-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ea549-104">Especifica uma cadeia de caracteres de comando, fornecida pelo usuário, que o método [Resync](resync-method-ado.md) emite para atualizar os dados na tabela chamada na propriedade dinâmica [Tabela exclusiva](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ea549-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ea549-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ea549-105">Settings and Return Values</span></span>

<span data-ttu-id="ea549-106">Define ou retorna um valor **String** que é uma sequência de comandos.</span><span class="sxs-lookup"><span data-stu-id="ea549-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea549-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea549-107">Remarks</span></span>

<span data-ttu-id="ea549-108">O objeto [Recordset](recordset-object-ado.md) é o resultado de um operação JOIN executada em diversas tabelas base.</span><span class="sxs-lookup"><span data-stu-id="ea549-108">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables.</span></span> <span data-ttu-id="ea549-109">As linhas afetadas dependem do parâmetro *AffectRecords* do método [Resync](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ea549-109">The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method.</span></span> <span data-ttu-id="ea549-110">O método **Resync** padrão é executado se as propriedades [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) e **Resync Command** não estiverem definidas.</span><span class="sxs-lookup"><span data-stu-id="ea549-110">The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="ea549-p102">A sequência de comandos da propriedade **Resync Command** é um comando com parâmetros ou um procedimento armazenado que identifica com exclusividade a linha que está sendo atualizada e retorna uma única linha contendo o mesmo número e ordem de colunas da linha a ser atualizada. A sequência de comandos contém um parâmetro para cada coluna de chave primária na **Unique Table**; caso contrário, um erro em tempo de execução será retornado. Os parâmetros são preenchidos automaticamente com os valores da chave primária da linha a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="ea549-p102">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed. The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned. The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="ea549-114">Aqui estão dois exemplos baseados no SQL:</span><span class="sxs-lookup"><span data-stu-id="ea549-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="ea549-115">O **Recordset** é definido por um comando:</span><span class="sxs-lookup"><span data-stu-id="ea549-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="ea549-116">A propriedade **Resync Command** é definida como:</span><span class="sxs-lookup"><span data-stu-id="ea549-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="ea549-p103">A **Unique Table** é *Orders* e sua chave primária, *OrderID*, está parametrizada. A subseleção fornece um modo simples de garantir de maneira programática que o mesmo número e a mesma ordem de colunas serão retornados da mesma forma que pelo comando original.</span><span class="sxs-lookup"><span data-stu-id="ea549-p103">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized. The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="ea549-119">O **Recordset** é definido por um procedimento armazenado:</span><span class="sxs-lookup"><span data-stu-id="ea549-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="ea549-120">O método **Resync** deve executar o seguinte procedimento armazenado:</span><span class="sxs-lookup"><span data-stu-id="ea549-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="ea549-121">A propriedade **Resync Command** é definida como:</span><span class="sxs-lookup"><span data-stu-id="ea549-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="ea549-122">Mais uma vez, a **Unique Table** é *Orders* e sua chave-primária, *OrderID*, está parametrizada.</span><span class="sxs-lookup"><span data-stu-id="ea549-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="ea549-123">**Resync Command** é uma propriedade dinâmica acrescentada à coleção **Properties** do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) estiver configurada como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="ea549-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

