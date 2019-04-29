---
title: Instrução ALTER TABLE (Microsoft Access SQL)
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b8bd9abac3aee8be8fe52e555fcd5247e804f258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297155"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="2c124-102">Instrução ALTER TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="2c124-102">ALTER TABLE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="2c124-103">**Aplica-se a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c124-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c124-104">Modifica o design de uma tabela depois de ter sido criada com a instrução [CREATE TABLE](create-table-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="2c124-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>

> [!NOTE]
> <span data-ttu-id="2c124-105">O mecanismo de banco de dados do Microsoft Access não oferece suporte para o uso da instrução ALTER TABLE, ou para quaisquer instruções da linguagem de definição de dados (DDL), com bancos de dados que não sejam do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2c124-105">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases.</span></span> <span data-ttu-id="2c124-106">Em vez disso, utilize os métodos DAO **Criar**.</span><span class="sxs-lookup"><span data-stu-id="2c124-106">Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c124-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c124-107">Syntax</span></span>

<span data-ttu-id="2c124-108">ALTER TABLE *tabela* {ADD {COLUMN *tipo de campo*\[(*tamanho*)\] \[NOT NULL\] \[CONSTRAINT *índice*\] | ALTER COLUMN *tipo de campo*\[(*tamanho*)\] | CONSTRAINT *índicedevárioscampos*} | DROP {COLUMN *campo* I CONSTRAINT *nomedoíndice*} }</span><span class="sxs-lookup"><span data-stu-id="2c124-108">ALTER TABLE table {ADD {COLUMN field type[(size)] [NOT NULL]     [CONSTRAINT index] | 
    ALTER COLUMN field type[(size)] | 
    CONSTRAINT multifieldindex} | 
    DROP {COLUMN field I CONSTRAINT indexname} }</span></span>

<span data-ttu-id="2c124-109">A instrução ALTER TABLE possui as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="2c124-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c124-110">Parte</span><span class="sxs-lookup"><span data-stu-id="2c124-110">Part</span></span></p></th>
<th><p><span data-ttu-id="2c124-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c124-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c124-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="2c124-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="2c124-113">O nome da tabela a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="2c124-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c124-114"><em>campo</em></span><span class="sxs-lookup"><span data-stu-id="2c124-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="2c124-p102">O nome do campo a ser adicionado ou excluído da <em>tabela</em>. Ou o nome do campo a ser alterado na <em>tabela</em>.</span><span class="sxs-lookup"><span data-stu-id="2c124-p102">The name of the field to be added to or deleted from <em>table</em>. Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c124-117"><em>tipo</em></span><span class="sxs-lookup"><span data-stu-id="2c124-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="2c124-118">O tipo de dados do <em>campo</em>.</span><span class="sxs-lookup"><span data-stu-id="2c124-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c124-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="2c124-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="2c124-120">O tamanho do campo em caracteres (somente os campos Texto e Binário).</span><span class="sxs-lookup"><span data-stu-id="2c124-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c124-121"><em>índice</em></span><span class="sxs-lookup"><span data-stu-id="2c124-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="2c124-122">O índice de <em>campo</em>.</span><span class="sxs-lookup"><span data-stu-id="2c124-122">The index for <em>field</em>.</span></span> <span data-ttu-id="2c124-123">Para saber mais sobre como construir o índice, confira a <a href="constraint-clause-microsoft-access-sql.md">cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="2c124-123">For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c124-124"><em>índicedevárioscampos</em></span><span class="sxs-lookup"><span data-stu-id="2c124-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="2c124-125">A definição de um índice de campos múltiplos a ser adicionado a <em>tabela</em>.</span><span class="sxs-lookup"><span data-stu-id="2c124-125">The definition of a multiple-field index to be added to <em>table</em>.</span></span> <span data-ttu-id="2c124-126">Para saber mais sobre como construir o índice, confira a <a href="constraint-clause-microsoft-access-sql.md">cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="2c124-126">For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c124-127"><em>nomedoíndice</em></span><span class="sxs-lookup"><span data-stu-id="2c124-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="2c124-128">O nome do índice de vários campos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2c124-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2c124-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c124-129">Remarks</span></span>

<span data-ttu-id="2c124-130">Ao usar a instrução ALTER TABLE, você pode alterar uma tabela existente de diversas maneiras.</span><span class="sxs-lookup"><span data-stu-id="2c124-130">Using the ALTER TABLE statement you can alter an existing table in several ways.</span></span> <span data-ttu-id="2c124-131">Você pode:</span><span class="sxs-lookup"><span data-stu-id="2c124-131">You can:</span></span>

- <span data-ttu-id="2c124-p106">Usar ADD COLUMN para adicionar um novo campo à tabela. Você especifica o nome do campo, o tipo de dados e (para os campos Texto e Binário) um tamanho opcional. Por exemplo, a seguinte instrução adiciona um campo Texto de 25 caracteres chamado Anotações à tabela Funcionários:</span><span class="sxs-lookup"><span data-stu-id="2c124-p106">Use ADD COLUMN to add a new field to the table. You specify the field name, data type, and (for Text and Binary fields) an optional size. For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  <span data-ttu-id="2c124-135">Você também pode definir um índice nesse campo.</span><span class="sxs-lookup"><span data-stu-id="2c124-135">You can also define an index on that field.</span></span> <span data-ttu-id="2c124-136">Para saber mais sobre índices de um único campo, confira a [cláusula CONSTRAINT](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="2c124-136">For more information on single-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
  <span data-ttu-id="2c124-137">Se você especificar um campo como NOT NULL, novos registros serão necessários para ter dados válidos nesse campo.</span><span class="sxs-lookup"><span data-stu-id="2c124-137">If you specify NOT NULL for a field then new records are required to have valid data in that field.</span></span>

- <span data-ttu-id="2c124-p108">Use ALTER COLUMN para alterar o tipo de dados de um campo existente. Você especifica o nome do campo, o novo tipo de dados e um tamanho opcional para os campos Texto e Binário. Por exemplo, a seguinte instrução altera o tipo de dados de um campo chamado CEP na tabela Funcionários (originalmente definido como Inteiro) para um campo Texto de 10 caracteres:</span><span class="sxs-lookup"><span data-stu-id="2c124-p108">Use ALTER COLUMN to change the data type of an existing field. You specify the field name, the new data type, and an optional size for Text and Binary fields. For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- <span data-ttu-id="2c124-141">Use ADD CONSTRAINT para adicionar um índice de campos múltiplos.</span><span class="sxs-lookup"><span data-stu-id="2c124-141">Use ADD CONSTRAINT to add a multiple-field index.</span></span> <span data-ttu-id="2c124-142">Para saber mais sobre índices de vários campos, confira a [cláusula CONSTRAINT](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="2c124-142">For more information on multiple-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>

- <span data-ttu-id="2c124-p110">Use DROP COLUMN para excluir um campo. Você especifica somente o nome do campo.</span><span class="sxs-lookup"><span data-stu-id="2c124-p110">Use DROP COLUMN to delete a field. You specify only the name of the field.</span></span>

- <span data-ttu-id="2c124-p111">Use DROP CONSTRAINT para excluir um índice de vários campos. Você especifica somente o nome do índice que segue a palavra reservada CONSTRAINT.</span><span class="sxs-lookup"><span data-stu-id="2c124-p111">Use DROP CONSTRAINT to delete a multiple-field index. You specify only the index name following the CONSTRAINT reserved word.</span></span>


> [!NOTE] 
> - <span data-ttu-id="2c124-147">Não é possível adicionar ou excluir mais de um campo ou índice por vez.</span><span class="sxs-lookup"><span data-stu-id="2c124-147">You cannot add or delete more than one field or index at a time.</span></span>
> - <span data-ttu-id="2c124-148">Você pode usar a instrução [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para adicionar um índice de campo único ou de vários campos a uma tabela, e pode usar as instruções ALTER TABLE ou [DROP](drop-statement-microsoft-access-sql.md) para excluir um índice criado com ALTER TABLE ou CREATE INDEX.</span><span class="sxs-lookup"><span data-stu-id="2c124-148">You can use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the [DROP](drop-statement-microsoft-access-sql.md) statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span>
> - <span data-ttu-id="2c124-149">Você pode usar NOT NULL em um único campo ou em uma cláusula nomeada CONSTRAINT que se aplica a um único campo ou a vários campos chamados CONSTRAINT.</span><span class="sxs-lookup"><span data-stu-id="2c124-149">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="2c124-150">No entanto, você pode aplicar a restrição NOT NULL apenas uma vez a um campo.</span><span class="sxs-lookup"><span data-stu-id="2c124-150">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="2c124-151">Tentar aplicar a restrição mais de uma vez acarretará um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2c124-151">Attempting to apply this restriction more than once restuls in a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="2c124-152">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2c124-152">Example</span></span>

<span data-ttu-id="2c124-153">Este exemplo adiciona um campo Salário com o tipo de dados **Dinheiro** à tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="2c124-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="2c124-154">Este exemplo altera o campo Salário do tipo de dados **Dinheiro** para o tipo de dados de **Caractere**.</span><span class="sxs-lookup"><span data-stu-id="2c124-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="2c124-155">Este exemplo remove o campo Salário da tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="2c124-155">This example removes the Salary field from the Employees table.</span></span>

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="2c124-p113">Este exemplo adiciona uma chave estrangeira à tabela Pedidos. A chave estrangeira é baseada no campo IDdoFuncionário e se refere ao campo IDdoFuncionário na tabela Funcionários. Neste exemplo, não é necessário listar o campo IDdoFuncionário depois da tabela Funcionários na cláusula REFERENCES, pois a IDdoFuncionário é a principal chave da tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="2c124-p113">This example adds a foreign key to the Orders table. The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table. In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="2c124-159">Este exemplo remove a chave estrangeira da tabela Pedidos.</span><span class="sxs-lookup"><span data-stu-id="2c124-159">This example removes the foreign key from the Orders table.</span></span>

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
