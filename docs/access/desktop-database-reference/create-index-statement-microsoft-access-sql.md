---
title: Instrução CREATE INDEX (Microsoft Access SQL)
TOCTitle: CREATE INDEX statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 46bc0a50e31555189c069e0ee09c4c84349c04c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295426"
---
# <a name="create-index-statement-microsoft-access-sql"></a><span data-ttu-id="afe85-102">Instrução CREATE INDEX (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="afe85-102">CREATE INDEX Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="afe85-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="afe85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="afe85-104">Cria um novo índice em uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="afe85-104">Creates a new index on an existing table.</span></span>

> [!NOTE]
> <span data-ttu-id="afe85-105">Para bancos de dados de mecanismo de banco de dados não Microsoft Access, o mecanismo de banco de dados Microsoft Access não fornece suporte ao uso de CREATE INDEX (exceto para criar um pseudo índice em uma tabela ODBC vinculada) nem de nenhuma instrução de linguagem de definição de dados (DDL).</span><span class="sxs-lookup"><span data-stu-id="afe85-105">For non-Microsoft Access atabse engine databases, the Microsoft Access database engine does not support the use of CREATE INDEX (except to create a pseudo index on an ODBC linked table) or any of the data definition language (DDL) statements.</span></span> <span data-ttu-id="afe85-106">Em vez disso, utilize os métodos DAO **Criar**.</span><span class="sxs-lookup"><span data-stu-id="afe85-106">Use the DAO Create methods instead.</span></span> <span data-ttu-id="afe85-107">Para mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="afe85-107">For more information, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe85-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afe85-108">Syntax</span></span>

<span data-ttu-id="afe85-109">CREATE \[ UNIQUE \] INDEX *índice* ON *tabela* (*campo* \[ASC|DESC\]\[, *campo* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]</span><span class="sxs-lookup"><span data-stu-id="afe85-109">CREATE [ UNIQUE ] INDEX index
    ON table (field [ASC|DESC][, field [ASC|DESC], …])
    [WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }]</span></span>

<span data-ttu-id="afe85-110">A instrução CREATE INDEX tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="afe85-110">The CREATE INDEX statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="afe85-111">Sair</span><span class="sxs-lookup"><span data-stu-id="afe85-111">Part</span></span></p></th>
<th><p><span data-ttu-id="afe85-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="afe85-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afe85-113"><em>índice</em></span><span class="sxs-lookup"><span data-stu-id="afe85-113"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="afe85-114">O nome do índice a ser criado.</span><span class="sxs-lookup"><span data-stu-id="afe85-114">The name of the index to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afe85-115"><em>tabela</em></span><span class="sxs-lookup"><span data-stu-id="afe85-115"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="afe85-116">O nome da tabela existente que conterá o índice.</span><span class="sxs-lookup"><span data-stu-id="afe85-116">The name of the existing table that will contain the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afe85-117"><em>campo</em></span><span class="sxs-lookup"><span data-stu-id="afe85-117"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="afe85-p102">O nome do(s) campo(s) a ser indexado. Para criar um índice de campo único, liste o nome do campo entre parênteses, após o nome da tabela. Para criar um índice de vários campos, liste o nome de cada campo a ser incluído no índice. Para criar índices em ordem decrescente, use a palavra reservada DESC; caso contrário, os índices serão considerados como crescente.</span><span class="sxs-lookup"><span data-stu-id="afe85-p102">The name of the field or fields to be indexed. To create a single-field index, list the field name in parentheses following the table name. To create a multiple-field index, list the name of each field to be included in the index. To create descending indexes, use the DESC reserved word; otherwise, indexes are assumed to be ascending.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="afe85-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="afe85-122">Remarks</span></span>

<span data-ttu-id="afe85-123">Para proibir valores duplicados nos campos indexados de registros diferentes, use a palavra reservada UNIQUE.</span><span class="sxs-lookup"><span data-stu-id="afe85-123">To prohibit duplicate values in the indexed field or fields of different records, use the UNIQUE reserved word.</span></span>

<span data-ttu-id="afe85-124">Na cláusula opcional WITH, você pode aplicar regras de validação de dados.</span><span class="sxs-lookup"><span data-stu-id="afe85-124">In the optional WITH clause you can enforce data validation rules.</span></span> <span data-ttu-id="afe85-125">Você pode:</span><span class="sxs-lookup"><span data-stu-id="afe85-125">You can:</span></span>

- <span data-ttu-id="afe85-126">Proibir entradas nulas nos campos indexados de novos registros, usando a opção DISALLOW NULL.</span><span class="sxs-lookup"><span data-stu-id="afe85-126">Prohibit Null entries in the indexed field or fields of new records by using the DISALLOW NULL option.</span></span>

- <span data-ttu-id="afe85-127">Impedir que registros com valores **Null** nos campos indexados sejam incluídos no índice, usando a opção IGNORE NULL.</span><span class="sxs-lookup"><span data-stu-id="afe85-127">Prevent records with **Null** values in the indexed field or fields from being included in the index by using the IGNORE NULL option.</span></span>

- <span data-ttu-id="afe85-p104">Designar o campo ou os campos indexados como a chave primária, utilizando a palavra reservada PRIMARY. Isso implica que a chave seja exclusiva, para que você possa omitir a palavra reservada UNIQUE.</span><span class="sxs-lookup"><span data-stu-id="afe85-p104">Designate the indexed field or fields as the primary key by using the PRIMARY reserved word. This implies that the key is unique, so you can omit the UNIQUE reserved word.</span></span>

<span data-ttu-id="afe85-130">Você pode usar CREATE INDEX para criar um pseudo índice em uma tabela vinculada em uma fonte de dados ODBC, como o Microsoft SQL Server, que ainda não tem um índice.</span><span class="sxs-lookup"><span data-stu-id="afe85-130">You can use CREATE INDEX to create a pseudo index on a linked table in an ODBC data source, such as Microsoft® SQL Server™, that does not already have an index.</span></span> <span data-ttu-id="afe85-131">Não é necessário ter permissão ou acesso ao servidor remoto para criar um pseudoíndice, e o banco de dados remoto reconhece a presença do pseudoíndice e não é afetado por ele.</span><span class="sxs-lookup"><span data-stu-id="afe85-131">You do not need permission or access to the remote server to create a pseudo index, and the remote database is unaware of and unaffected by the pseudo index.</span></span> <span data-ttu-id="afe85-132">Use a mesma sintaxe para tabelas vinculadas e nativas.</span><span class="sxs-lookup"><span data-stu-id="afe85-132">You use the same syntax for both linked and native tables.</span></span> <span data-ttu-id="afe85-133">Pode ser especialmente útil criar um pseudoíndice em uma tabela que normalmente seria somente leitura.</span><span class="sxs-lookup"><span data-stu-id="afe85-133">Creating a pseudo-index on a table that would ordinarily be read-only can be especially useful.</span></span>

<span data-ttu-id="afe85-134">Também é possível usar a instrução [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para adicionar um índice de único arquivo ou de vários arquivos a uma tabela, e a instrução ALTER TABLE ou [DROP](drop-statement-microsoft-access-sql.md) para remover um índice criado com ALTER TABLE ou CREATE INDEX.</span><span class="sxs-lookup"><span data-stu-id="afe85-134">You can also use the [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use the ALTER TABLE statement or the [DROP](drop-statement-microsoft-access-sql.md) statement to remove an index created with ALTER TABLE or CREATE INDEX.</span></span>

> [!NOTE]
> <span data-ttu-id="afe85-135">Não use a palavra reservada PRIMARY ao criar um novo índice em uma tabela que já tem uma chave primária; se você fizer isso, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="afe85-135">Do not use the PRIMARY reserved word when you create a new index on a table that already has a primary key; if you do, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="afe85-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="afe85-136">Example</span></span>

<span data-ttu-id="afe85-137">Este exemplo cria um índice que consiste nos campos Telefone Residencial e Ramal na tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="afe85-137">This example creates an index consisting of the fields Home Phone and Extension in the Employees table.</span></span>

```vb
    Sub CreateIndexX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create the NewIndex index on the Employees table. 
        dbs.Execute "CREATE INDEX NewIndex ON Employees " _ 
            & "(HomePhone, Extension);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="afe85-p106">Este exemplo cria um índice na tabela Customers utilizando o campo CustomerID. Dois registros não podem ter os mesmos dados no campo CustomerID e nenhum valor nulo é permitido.</span><span class="sxs-lookup"><span data-stu-id="afe85-p106">This example creates an index on the Customers table using the CustomerID field. No two records can have the same data in the CustomerID field, and no Null values are allowed.</span></span>

```vb
    Sub CreateIndexX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a unique index, CustID, on the  
        ' CustomerID field. 
        dbs.Execute "CREATE UNIQUE INDEX CustID " _ 
            & "ON Customers (CustomerID) " _ 
            & "WITH DISALLOW NULL;" 
     
        dbs.Close 
     
    End Sub
```
