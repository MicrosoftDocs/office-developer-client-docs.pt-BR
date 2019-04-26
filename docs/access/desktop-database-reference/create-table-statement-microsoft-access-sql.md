---
title: Instrução CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 296e1405245d6204d136888e78b6a3846b468a1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295356"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="50494-102">Instrução CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="50494-102">CREATE TABLE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="50494-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50494-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50494-104">Cria uma nova tabela.</span><span class="sxs-lookup"><span data-stu-id="50494-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="50494-105">O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE TABLE ou de qualquer uma das instruções DDL com bancos de dados de mecanismos de banco de dados que não são do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="50494-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="50494-106">Em vez disso, utilize os métodos DAO **Criar**.</span><span class="sxs-lookup"><span data-stu-id="50494-106">Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="50494-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50494-107">Syntax</span></span>

<span data-ttu-id="50494-108">CREATE \[TEMPORARY\] TABLE *tabela* (*campo1 tipo* \[(*tamanho*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*índice1*\] \[, *campo2* *tipo* \[(*tamanho*)\] \[NOT NULL\] \[*índice2*\] \[, …\]\] \[, CONSTRAINT *índicedevárioscampos* \[, …\]\])</span><span class="sxs-lookup"><span data-stu-id="50494-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="50494-109">A instrução CREATE TABLE tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="50494-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50494-110">Sair</span><span class="sxs-lookup"><span data-stu-id="50494-110">Part</span></span></p></th>
<th><p><span data-ttu-id="50494-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="50494-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50494-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="50494-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="50494-113">O nome da tabela a ser criada.</span><span class="sxs-lookup"><span data-stu-id="50494-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50494-114"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="50494-114"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="50494-p102">O nome do campo ou campos a serem criados na nova tabela. Crie pelo menos um campo.</span><span class="sxs-lookup"><span data-stu-id="50494-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50494-117"><em>tipo</em></span><span class="sxs-lookup"><span data-stu-id="50494-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="50494-118">O tipo de dados do <em>campo</em> na nova tabela.</span><span class="sxs-lookup"><span data-stu-id="50494-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50494-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="50494-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="50494-120">O tamanho do campo em caracteres (somente os campos Texto e Binário).</span><span class="sxs-lookup"><span data-stu-id="50494-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50494-121"><em>índice1</em>, <em>índice2</em></span><span class="sxs-lookup"><span data-stu-id="50494-121"><em>index1</em>  ,  <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="50494-122">Uma cláusula CONSTRAINT definindo um índice de campo único.</span><span class="sxs-lookup"><span data-stu-id="50494-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="50494-123">Para mais informações sobre como criar esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="50494-123">For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50494-124"><em>índicedevárioscampos</em></span><span class="sxs-lookup"><span data-stu-id="50494-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="50494-125">Uma cláusula CONSTRAINT definindo um índice de vários campos.</span><span class="sxs-lookup"><span data-stu-id="50494-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="50494-126">Para mais informações sobre como criar esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</span><span class="sxs-lookup"><span data-stu-id="50494-126">For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="50494-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="50494-127">Remarks</span></span>

<span data-ttu-id="50494-128">Use a instrução CREATE TABLE para definir uma nova tabela e seus campos e restrições de campo.</span><span class="sxs-lookup"><span data-stu-id="50494-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="50494-129">Se NOT NULL for especificado para um campo, então será necessário que novos registros tenham dados válidos nesse campo.</span><span class="sxs-lookup"><span data-stu-id="50494-129">If NOT NULL is specified for a field, then new records are required to have valid data in that field.</span></span>

<span data-ttu-id="50494-p106">Uma cláusula CONSTRAINT estabelece várias restrições sobre um campo e pode ser usada para estabelecer a chave primária. É possível também utilizar a instrução [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para criar uma chave primária ou índices extras em tabelas existentes.</span><span class="sxs-lookup"><span data-stu-id="50494-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="50494-p107">Você pode usar NOT NULL em um único campo ou em uma cláusula nomeada CONSTRAINT que se aplica a um único campo ou a vários campos chamados CONSTRAINT. No entanto, você pode aplicar a restrição NOT NULL apenas uma vez a um campo. Tentar aplicar a restrição mais de uma vez acarretará um erro de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="50494-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="50494-135">Quando uma tabela TEMPORARY for criada, ela será visível somente na sessão em que for criada.</span><span class="sxs-lookup"><span data-stu-id="50494-135">When a TEMPORARY table is created it is visible only within the session in which it was created.</span></span> <span data-ttu-id="50494-136">Ela será excluída automaticamente quando a sessão for encerrada.</span><span class="sxs-lookup"><span data-stu-id="50494-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="50494-137">As tabelas temporárias podem ser acessadas por mais de um usuário.</span><span class="sxs-lookup"><span data-stu-id="50494-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="50494-138">O atributo WITH COMPRESSION pode ser usado somente com os tipos de dados CHARACTER e MEMO (também conhecidos como TEXT) e seus sinônimos.</span><span class="sxs-lookup"><span data-stu-id="50494-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="50494-139">O atributo WITH COMPRESSION foi adicionado para as colunas de CHARACTER devido à alteração para o formato de representação de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="50494-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="50494-140">Os caracteres Unicode exigem uniformemente dois bytes para cada caractere.</span><span class="sxs-lookup"><span data-stu-id="50494-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="50494-141">Para os bancos de dados existentes do Microsoft Jet que contêm predominantemente dados de caracteres, isso pode significar que o arquivo de banco de dados poderá dobrar de tamanho quando for convertido para o formato do mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="50494-141">For existing Microsoft® Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="50494-142">No entanto, a representação Unicode de vários conjuntos de caracteres, aqueles anteriormente indicados como Conjuntos de Caracteres de um Byte (SBCS), poderá ser facilmente compactada para um único byte.</span><span class="sxs-lookup"><span data-stu-id="50494-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS) can easily be compressed to a single byte.</span></span> <span data-ttu-id="50494-143">Se você definir uma coluna CHARACTER com esse atributo, os dados serão compactados automaticamente ao serem armazenados e descompactados quando recuperados da coluna.</span><span class="sxs-lookup"><span data-stu-id="50494-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="50494-p110">As colunas MEMO também podem ser definidas para armazenar dados em um formato compactado. No entanto, há uma limitação. Somente as instâncias de colunas MEMO, quando compactadas, caberão em 4096 bytes ou menos, serão compactadas. Todas as instâncias de colunas MEMO permanecerão descompactadas. Isso significa que em uma determinada tabela, para uma determinada coluna MEMO, alguns dados poderão ser compactados e alguns dados poderão não ser compactados.</span><span class="sxs-lookup"><span data-stu-id="50494-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="50494-149">Exemplo</span><span class="sxs-lookup"><span data-stu-id="50494-149">Example</span></span>

<span data-ttu-id="50494-150">Este exemplo cria uma nova tabela chamada ThisTable com dois campos de texto.</span><span class="sxs-lookup"><span data-stu-id="50494-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="50494-151">Este exemplo cria uma nova tabela chamada Mytable com dois campos de texto, um campo Data/Hora e um índice exclusivo composto por todos os três campos.</span><span class="sxs-lookup"><span data-stu-id="50494-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="50494-p111">Este exemplo cria uma nova tabela com dois campos de texto e um campo **Inteiro**.O campo CPF é a chave primária.</span><span class="sxs-lookup"><span data-stu-id="50494-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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
