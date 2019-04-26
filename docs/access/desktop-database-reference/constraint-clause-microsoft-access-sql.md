---
title: Cláusula de RESTRIÇÃO (Microsoft Access SQL)
TOCTitle: CONSTRAINT clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 356620376658bb927c690056f4de9a01554aa47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295643"
---
# <a name="constraint-clause-microsoft-access-sql"></a><span data-ttu-id="b5692-102">Cláusula de RESTRIÇÃO (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b5692-102">CONSTRAINT Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="b5692-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5692-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5692-104">Uma restrição é semelhante a um índice, embora possa ser usada para estabelecer uma relação com outra tabela.</span><span class="sxs-lookup"><span data-stu-id="b5692-104">A constraint is similar to an index, although it can also be used to establish a relationship with another table.</span></span>

<span data-ttu-id="b5692-p101">Use a cláusula CONSTRAINT em instruções [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) e [CREATE TABLE](create-table-statement-microsoft-access-sql.md) para criar ou excluir restrições. Existem dois tipos de cláusula CONSTRAINT: uma para criação de uma restrição em um campo único e outra para criação de mais de um campo.</span><span class="sxs-lookup"><span data-stu-id="b5692-p101">You use the CONSTRAINT clause in [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) and [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statements to create or delete constraints. There are two types of CONSTRAINT clauses: one for creating a constraint on a single field and one for creating a constraint on more than one field.</span></span>

> [!NOTE]
> <span data-ttu-id="b5692-107">O mecanismo de banco de dados do Microsoft Access não suporta o uso de CONSTRAINT ou de nenhuma das instruções DDL (Data Definition Language) com bancos de dados do mecanismo de bancos de dados de terceiros.</span><span class="sxs-lookup"><span data-stu-id="b5692-107">The Microsoft Access database engine does not support the use of CONSTRAINT, or any of the data definition language (DDL) statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="b5692-108">Em vez disso, utilize os métodos DAO **Criar**.</span><span class="sxs-lookup"><span data-stu-id="b5692-108">Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5692-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5692-109">Syntax</span></span>

### <a name="single-field-constraint"></a><span data-ttu-id="b5692-110">Restrição de campo único:</span><span class="sxs-lookup"><span data-stu-id="b5692-110">Single-field constraint:</span></span>

<span data-ttu-id="b5692-111">RESTRIÇÃO*nome* {CHAVE PRIMÁRIA | EXCLUSIVA | NÃO NULO | REFERÊNCIAS *tabelaestrangeira* \[(*campoestrangeiro1, campoestrangeiro2*)\] \[A ATUALIZAR CASCATA | DEFINIR NULO \] \[A DELETAR CASCATA | DEFINIR NULO \]}</span><span class="sxs-lookup"><span data-stu-id="b5692-111">CONSTRAINT name {PRIMARY KEY | UNIQUE | NOT NULL |
    REFERENCES foreigntable [(foreignfield1, foreignfield2)]
    [ON UPDATE CASCADE | SET NULL]
    [ON DELETE CASCADE | SET NULL]}</span></span>

### <a name="multiple-field-constraint"></a><span data-ttu-id="b5692-112">Restrição de vários campos:</span><span class="sxs-lookup"><span data-stu-id="b5692-112">Multiple-field constraint:</span></span>

<span data-ttu-id="b5692-113">RESTRIÇÃO*nome* {CHAVE PRIMÁRIA (*primária1*\[, *primária2* \[, …\]\]) | EXCLUSIVA (*exclusiva1*\[, *exclusiva2* \[, …\]\]) | NÃO NULO (*nãonulo1*\[, *nãonulo2* \[, …\]\]) | CHAVE ESTRANGEIRA \[NENHUM ÍNDICE\] (*ref1*\[, *ref2* \[, …\]\]) REFERÊNCIAS *tabelaestrangeira* \[(*campoestrangeiro1* \[, *campoestrangeiro2* \[, …\]\])\] \[A ATUALIZAR CASCATA | DEFINIR NULO\] \[A DELETAR CASCATA | DEFINIR NULO\]}</span><span class="sxs-lookup"><span data-stu-id="b5692-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="b5692-114">A cláusula CONSTRAINT tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="b5692-114">The CONSTRAINT clause has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5692-115">Sair</span><span class="sxs-lookup"><span data-stu-id="b5692-115">Part</span></span></p></th>
<th><p><span data-ttu-id="b5692-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5692-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5692-117"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="b5692-117"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="b5692-118">O nome da restrição a ser criada.</span><span class="sxs-lookup"><span data-stu-id="b5692-118">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5692-119"><em>primária1</em>, <em>primária2</em></span><span class="sxs-lookup"><span data-stu-id="b5692-119"><em>primary1</em>, <em>primary2</em></span></span></p></td>
<td><p><span data-ttu-id="b5692-120">O nome do campo ou dos campos que será designado como a chave primária.</span><span class="sxs-lookup"><span data-stu-id="b5692-120">The name of the field or fields to be designated the primary key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5692-121"><em>exclusiva1</em>, <em>exclusiva2</em></span><span class="sxs-lookup"><span data-stu-id="b5692-121"><em>unique1</em>, <em>unique2</em></span></span></p></td>
<td><p><span data-ttu-id="b5692-122">O nome dos campos que serão designados como uma chave exclusiva.</span><span class="sxs-lookup"><span data-stu-id="b5692-122">The name of the field or fields to be designated as a unique key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5692-123"><em>nãonulo1, nãonulo2</em></span><span class="sxs-lookup"><span data-stu-id="b5692-123"><em>notnull1, notnull2</em></span></span></p></td>
<td><p><span data-ttu-id="b5692-124">O nome dos campos restritos a valores não nulos.</span><span class="sxs-lookup"><span data-stu-id="b5692-124">The name of the field or fields that are restricted to non-Null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5692-125"><em>ref1</em>, <em>ref2</em></span><span class="sxs-lookup"><span data-stu-id="b5692-125"><em>ref1</em>, <em>ref2</em></span></span></p></td>
<td><p><span data-ttu-id="b5692-126">O nome de um campo ou campos de chave estrangeira que se refere a campos em outra tabela.</span><span class="sxs-lookup"><span data-stu-id="b5692-126">The name of a foreign key field or fields that refer to fields in another table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5692-127"><em>tabelaestrangeira</em></span><span class="sxs-lookup"><span data-stu-id="b5692-127"><em>foreigntable</em></span></span></p></td>
<td><p><span data-ttu-id="b5692-128">O nome da tabela externa que contém o campo ou os campos especificado por <em>foreignfield</em>.</span><span class="sxs-lookup"><span data-stu-id="b5692-128">The name of the foreign table containing the field or fields specified by <em>foreignfield</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5692-129"><em>campoestrangeiro1</em>, <em>campoestrangeiro2</em></span><span class="sxs-lookup"><span data-stu-id="b5692-129"><em>foreignfield1</em>, <em>foreignfield2</em></span></span></p></td>
<td><p><span data-ttu-id="b5692-p103">O nome dos campos em <em>tabelaestrangeira</em> especificados por <em>ref1</em>, <em>ref2</em>. Você poderá omitir essa cláusula se o campo de referência for a chave primária de <em>tabelaestrangeira</em>.</span><span class="sxs-lookup"><span data-stu-id="b5692-p103">The name of the field or fields in <em>foreigntable</em> specified by <em>ref1</em>, <em>ref2</em>. You can omit this clause if the referenced field is the primary key of <em>foreigntable</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b5692-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5692-132">Remarks</span></span>

<span data-ttu-id="b5692-133">Use a sintaxe para uma restrição de campo único na cláusula de definição de campo de uma instrução ALTER TABLE ou CREATE TABLE, imediatamente após a especificação do tipo de dado do campo.</span><span class="sxs-lookup"><span data-stu-id="b5692-133">You use the syntax for a single-field constraint in the field-definition clause of an ALTER TABLE or CREATE TABLE statement immediately following the specification of the field's data type.</span></span>

<span data-ttu-id="b5692-134">Use a sintaxe de restrição de vários campos sempre que usar a palavra reservada CONSTRAINT fora da cláusula de definição de campo em uma instrução de ALTER TABLE ou CREATE TABLE.</span><span class="sxs-lookup"><span data-stu-id="b5692-134">You use the syntax for a multiple-field constraint whenever you use the reserved word CONSTRAINT outside a field-definition clause in an ALTER TABLE or CREATE TABLE statement.</span></span>

<span data-ttu-id="b5692-135">Com CONSTRAINT, você pode designar um campo como um dos seguintes tipos de restrições:</span><span class="sxs-lookup"><span data-stu-id="b5692-135">Using CONSTRAINT you can designate a field as one of the following types of constraints:</span></span>

- <span data-ttu-id="b5692-p104">Você pode usar a palavra reservada UNIQUE para designar um campo como uma chave exclusiva. Isso significa que nenhum registro da tabela terá o mesmo valor nesse campo. Você pode restringir qualquer campo ou lista de campos como exclusivo. Se uma restrição de campos múltiplos for designada como uma chave exclusiva, os valores combinados de todos os campos no índice deverão ser exclusivos, mesmo que dois ou mais registros tenham o mesmo valor em apenas um dos campos.</span><span class="sxs-lookup"><span data-stu-id="b5692-p104">You can use the UNIQUE reserved word to designate a field as a unique key. This means that no two records in the table can have the same value in this field. You can constrain any field or list of fields as unique. If a multiple-field constraint is designated as a unique key, the combined values of all fields in the index must be unique, even if two or more records have the same value in just one of the fields.</span></span>

- <span data-ttu-id="b5692-p105">Você pode usar as palavras reservadas PRIMARY KEY para designar um campo ou um conjunto de campos em uma tabela como chave primária. Todos os valores de chave primária devem ser exclusivos e não **nulos**, e pode haver apenas uma chave primária em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="b5692-p105">You can use the PRIMARY KEY reserved words to designate one field or set of fields in a table as a primary key. All values in the primary key must be unique and not **Null**, and there can be only one primary key for a table.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="b5692-142">Não defina uma restrição PRIMARY KEY em uma tabela que já tem uma chave primária; se você fizer isso, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="b5692-142">Do not set a PRIMARY KEY constraint on a table that already has a primary key; if you do, an error occurs.</span></span>

- <span data-ttu-id="b5692-p106">Use as palavras reservadas FOREIGN KEY para designar um campo como uma chave estrangeira. Se a chave primária da tabela externa for composta de mais de um campo, use uma definição de restrição de campo múltiplo, listando todos os campos de referência, o nome da tabela externa e os nomes dos campos referenciados na tabela externa, na mesma ordem em que estão listados os campos de referência. Se o campo ou os campos de referência forem a chave primária da tabela externa, não será necessário especificar os campos referenciados. Por padrão, o mecanismo de banco de dados se comporta como se a chave primária da tabela externa fosse os campos referenciados. As restrições da chave estrangeira definem ações específicas que serão executadas quando for alterado um valor de chave primária correspondente:</span><span class="sxs-lookup"><span data-stu-id="b5692-p106">You can use the FOREIGN KEY reserved words to designate a field as a foreign key. If the foreign table's primary key consists of more than one field, you must use a multiple-field constraint definition, listing all of the referencing fields, the name of the foreign table, and the names of the referenced fields in the foreign table in the same order that the referencing fields are listed. If the referenced field or fields are the foreign table's primary key, you do not have to specify the referenced fields. By default the database engine behaves as if the foreign table's primary key is the referenced fields. Foreign key constraints define specific actions to be performed when a corresponding primary key value is changed:</span></span>

- <span data-ttu-id="b5692-p107">É possível especificar as ações a serem executadas na tabela estrangeira com base em uma ação correspondente realizada em uma chave primária na tabela em que CONSTRAINT é definida. Por exemplo, considere a seguinte definição da tabela Customers (Clientes):</span><span class="sxs-lookup"><span data-stu-id="b5692-p107">You can specify actions to be performed on the foreign table based on a corresponding action performed on a primary key in the table on which the CONSTRAINT is defined. For example, consider the following definition for the table Customers:</span></span>
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  <span data-ttu-id="b5692-150">Considere a seguinte definição da tabela Orders (Pedidos), que define uma relação de chave estrangeira que faz referência à chave primária da tabela Customers:</span><span class="sxs-lookup"><span data-stu-id="b5692-150">Consider the following definition of the table Orders, which defines a foreign key relationship referencing the primary key of the Customers table:</span></span>
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  <span data-ttu-id="b5692-p108">Ambas as cláusulas ON UPDATE CASCADE e ON DELETE CASCADE estão definidas na chave estrangeira. A cláusula ON UPDATE CASCADE significa que, se um identificador de cliente (CustId) for atualizado na tabela Customer, a atualização será feita em cascata na tabela Orders. Cada pedido que tiver um valor identificador de cliente correspondente será atualizado automaticamente com o novo valor. A cláusula ON DELETE CASCADE significa que, se um cliente for excluído da tabela Customer, todas as linhas da tabela Orders que contenham o mesmo valor identificador de cliente também serão excluídas. Considere as seguintes definições diferentes da tabela Orders, usando a ação SET NULL em vez da ação CASCADE:</span><span class="sxs-lookup"><span data-stu-id="b5692-p108">Both an ON UPDATE CASCADE and an ON DELETE CASCADE clause are defined on the foreign key. The ON UPDATE CASCADE clause means that if a customer's identifier (CustId) is updated in the Customer table, the update will be cascaded through the Orders table. Each order containing a corresponding customer identifier value will be updated automatically with the new value. The ON DELETE CASCADE clause means that if a customer is deleted from the Customer table, all rows in the Orders table containing the same customer identifier value will also be deleted. Consider the following different definition of the table Orders, using the SET NULL action instead of the CASCADE action:</span></span>
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  <span data-ttu-id="b5692-p109">A cláusula ON UPDATE SET NULL significa que, se o identificador do cliente (CustId) for atualizado na tabela Customer, os valores de chave estrangeira correspondentes na tabela Orders serão definidos automaticamente como NULL. Da mesma forma, a cláusula ON DELETE SET NULL significa que, se um cliente for excluído na tabela Customer, todas as chaves estrangeiras correspondentes na tabela Orders serão definidas automaticamente como NULL.</span><span class="sxs-lookup"><span data-stu-id="b5692-p109">The ON UPDATE SET NULL clause means that if a customer's identifier (CustId) is updated in the Customer table, the corresponding foreign key values in the Orders table will automatically be set to NULL. Similarly, the ON DELETE SET NULL clause means that if a customer is deleted from the Customer table, all corresponding foreign keys in the Orders table will automatically be set to NULL.</span></span>

<span data-ttu-id="b5692-p110">Para impedir a criação automática de índices para chaves estrangeiras, é possível usar o modificador NO INDEX. Essa forma de definição de chave estrangeira deve ser usada somente em casos em que os valores de índice resultantes seriam duplicados com frequência. Nos casos em que os valores de um índice de chave estrangeira são duplicados com frequência, o uso de um índice pode ser menos eficaz do que simplesmente executar uma verificação de tabela. Manter esse tipo de índice, com linhas inseridas e excluídas da tabela, reduz o desempenho e não oferece benefícios.</span><span class="sxs-lookup"><span data-stu-id="b5692-p110">To prevent the automatic creation of indexes for foreign keys, the modifier NO INDEX can be used. This form of foreign key definition should be used only in cases where the resulting index values would be frequently duplicated. Where the values in a foreign key index are frequently duplicated, using an index can be less efficient than simply performing a table scan. Maintaining this type of index, with rows inserted and deleted from the table, degrades performance and does not provide any benefit.</span></span>

## <a name="example"></a><span data-ttu-id="b5692-162">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b5692-162">Example</span></span>

<span data-ttu-id="b5692-163">Este exemplo cria uma nova tabela chamada ThisTable com dois campos de texto.</span><span class="sxs-lookup"><span data-stu-id="b5692-163">This example creates a new table called ThisTable with two text fields.</span></span>

```vb 
 Sub CreateTableX1()    
Dim dbs As Database 
 
    ' Modify this line to include the path to Northwind 
    ' on your computer. 
    Set dbs = OpenDatabase("Northwind.mdb") 
 
    ' Create a table with two text fields. 
    dbs.Execute "CREATE TABLE ThisTable " _ 
        & "(FirstName CHAR, LastName CHAR);" 
 
    dbs.Close 
 
End Sub
```

<br/>

<span data-ttu-id="b5692-164">Este exemplo cria uma nova tabela chamada Mytable com dois campos de texto, um campo Data/Hora e um índice exclusivo composto por todos os três campos.</span><span class="sxs-lookup"><span data-stu-id="b5692-164">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="b5692-p111">Este exemplo cria uma nova tabela com dois campos de texto e um campo **Inteiro**.O campo CPF é a chave primária.</span><span class="sxs-lookup"><span data-stu-id="b5692-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

