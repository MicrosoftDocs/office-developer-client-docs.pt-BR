---
title: Instrução CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE Statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 749d593a0c9ed32290ee91aec20c79a141a83f56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463611"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="00ec7-102">Instrução CREATE TABLE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="00ec7-102">CREATE TABLE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="00ec7-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="00ec7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00ec7-104">Cria uma nova tabela.</span><span class="sxs-lookup"><span data-stu-id="00ec7-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="00ec7-p101">[!OBSERVAçãO] O mecanismo do banco de dados do Microsoft Access não suporta o uso da instrução CREATE TABLE ou de quaisquer das instruções DDL com mecanismos de bancos de dados que não sejam do Microsoft Access. Em vez disso, use os métodos Create DAO.</span><span class="sxs-lookup"><span data-stu-id="00ec7-p101">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ec7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00ec7-107">Syntax</span></span>

<span data-ttu-id="00ec7-108">CRIAR \[temporário\] tabela *tabela* (*tipo field1* \[(*tamanho*)\] \[NOT NULL\] \[WITH COMPRESSION | COM COMPOSIÇÃO\] \[ *index1* \] \[, *field2* *tipo* \[(*tamanho*)\] \[NOT NULL\] \[ *índice 2* \] \[,... \] \] \[, Restrição *multifieldindex* \[,... \]\])</span><span class="sxs-lookup"><span data-stu-id="00ec7-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="00ec7-109">A instrução CREATE TABLE contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="00ec7-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00ec7-110">Parte</span><span class="sxs-lookup"><span data-stu-id="00ec7-110">Part</span></span></p></th>
<th><p><span data-ttu-id="00ec7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="00ec7-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00ec7-112"><em>tabela</em></span><span class="sxs-lookup"><span data-stu-id="00ec7-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="00ec7-113">O nome da tabela a ser criado.</span><span class="sxs-lookup"><span data-stu-id="00ec7-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ec7-114"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="00ec7-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="00ec7-p102">O nome do campo ou dos campos a serem criados na nova tabela. É necessário criar pelo menos um campo.</span><span class="sxs-lookup"><span data-stu-id="00ec7-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ec7-117"><em>tipo</em></span><span class="sxs-lookup"><span data-stu-id="00ec7-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="00ec7-118">O tipo de dados do <em>campo</em> na nova tabela.</span><span class="sxs-lookup"><span data-stu-id="00ec7-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ec7-119"><em>tamanho</em></span><span class="sxs-lookup"><span data-stu-id="00ec7-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="00ec7-120">O tamanho do campo em caracteres (somente campos de texto e campos binários).</span><span class="sxs-lookup"><span data-stu-id="00ec7-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ec7-121"><em>índice1</em>, <em>índice2</em></span><span class="sxs-lookup"><span data-stu-id="00ec7-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="00ec7-p103">Uma cláusula CONSTRAINT definindo um índice de campo único. Para obter mais informações sobre como criar esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.  </span><span class="sxs-lookup"><span data-stu-id="00ec7-p103">A CONSTRAINT clause defining a single-field index. For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ec7-124"><em>índicecomváriasids</em></span><span class="sxs-lookup"><span data-stu-id="00ec7-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="00ec7-p104">Uma cláusula CONSTRAINT definindo um índice de campos múltiplos. Para obter mais informações sobre como criar esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.  </span><span class="sxs-lookup"><span data-stu-id="00ec7-p104">A CONSTRAINT clause defining a multiple-field index. For more information on how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="00ec7-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="00ec7-127">Remarks</span></span>

<span data-ttu-id="00ec7-p105">Utilize a instrução CREATE TABLE para definir uma nova tabela e seus campos, além das restrições de campo. Se for especificado NOT NULL para um campo, então será necessário que os novos registros tenham dados válidos nesse campo.</span><span class="sxs-lookup"><span data-stu-id="00ec7-p105">Use the CREATE TABLE statement to define a new table and its fields and field constraints. If NOT NULL is specified for a field, then new records are required to have valid data in that field.</span></span>

<span data-ttu-id="00ec7-p106">Uma cláusula CONSTRAINT estabelece várias restrições sobre um campo e pode ser usada para estabelecer a chave primária. É possível também utilizar a instrução [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para criar uma chave primária ou índices extras em tabelas existentes.</span><span class="sxs-lookup"><span data-stu-id="00ec7-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="00ec7-p107">Você poderá usar NOT NULL em um campo único ou dentro de uma cláusula CONSTRAINT nomeada, que se aplica a um campo único ou a um campo múltiplo. No entanto, é possível aplicar a restrição NOT NULL a um campo somente uma vez. A tentativa de aplicar esta restrição mais de uma vez resultará em um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="00ec7-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="00ec7-p108">Quando uma tabela temporária for criada, ela será visível somente na sessão em que for criada. Ela será excluída automaticamente, ao encerrar a sessão. Essas tabelas podem ser acessadas por mais de um usuário.</span><span class="sxs-lookup"><span data-stu-id="00ec7-p108">When a TEMPORARY table is created it is visible only within the session in which it was created. It is automatically deleted when the session is terminated. Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="00ec7-138">O atributo WITH COMPRESSION pode ser utilizado com os tipos de dados Caractere e Memorando (também conhecido como Texto) e seus sinônimos.</span><span class="sxs-lookup"><span data-stu-id="00ec7-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="00ec7-p109">O atributo WITH COMPRESSION foi adicionado às colunas Caracteres por causa da alteração para o formato de representação de caracteres Unicode. Os caracteres Unicode exigem dois bytes uniformemente para cada caractere. Para os bancos de dados existentes do Microsoft® Jet, que contêm predominantemente dados de caracteres, isso pode significar que o arquivo de banco de dados poderá dobrar de tamanho quando for convertido para o formato do mecanismo de banco de dados do Microsoft Access. No entanto, a representação Unicode de vários conjuntos de caracteres, aqueles anteriormente indicados como conjuntos de caracteres de um byte (SBCS), poderá ser facilmente compactada para um único byte. Se definir uma coluna Caractere com esse atributo, os dados serão automaticamente compactados, à medida que forem armazenados e descompactados, ao serem resgatados de uma coluna.</span><span class="sxs-lookup"><span data-stu-id="00ec7-p109">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format. Unicode characters uniformly require two bytes for each character. For existing Microsoft® Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format. However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS) can easily be compressed to a single byte. If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="00ec7-p110">As colunas Memorando também podem ser definidas para armazenar dados em formato compactado. No entanto, existe uma limitação. Somente as instâncias de colunas Memorando que tiverem 4096 bytes ou menos serão compactadas. Todas as outras instâncias de colunas Memorando permanecerão descompactadas. Isso significa que, dentro de uma determinada tabela, para uma determinada coluna Memorando, alguns dados podem ser compactados e outros não.</span><span class="sxs-lookup"><span data-stu-id="00ec7-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="00ec7-149">Exemplo</span><span class="sxs-lookup"><span data-stu-id="00ec7-149">Example</span></span>

<span data-ttu-id="00ec7-150">Este exemplo cria uma nova tabela chamada ThisTable com dois campos de texto.</span><span class="sxs-lookup"><span data-stu-id="00ec7-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="00ec7-151">Este exemplo cria uma nova tabela chamada Mytable com dois campos de texto, um campo Data/Hora e um índice exclusivo composto por todos os três campos.</span><span class="sxs-lookup"><span data-stu-id="00ec7-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="00ec7-p111">Este exemplo cria uma nova tabela com dois campos de texto e um campo **Inteiro**.O campo CPF é a chave primária.</span><span class="sxs-lookup"><span data-stu-id="00ec7-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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
