---
title: Instrução CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/03/2019
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: dfcbbd55f2d20589849f63f260d40b507c8639f1
ms.sourcegitcommit: b27eedbc4538f78ee15134bf19abbc319605c3bc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2019
ms.locfileid: "36706170"
---
# <a name="create-table-statement-microsoft-access-sql"></a>Instrução CREATE TABLE (Microsoft Access SQL)

**Aplica-se ao**: Access 2013, Office 2013

Cria uma nova tabela.

> [!NOTE]
> O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE TABLE ou de qualquer uma das instruções DDL com bancos de dados de mecanismos de banco de dados que não são do Microsoft Access. Em vez disso, utilize os métodos DAO **Criar**.

## <a name="syntax"></a>Sintaxe

CREATE \[TEMPORARY\] TABLE *tabela* (*campo1 tipo* \[(*tamanho*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*índice1*\] \[, *campo2* *tipo* \[(*tamanho*)\] \[NOT NULL\] \[*índice2*\] \[, …\]\] \[, CONSTRAINT *índicedevárioscampos* \[, …\]\])

A instrução CREATE TABLE tem as seguintes partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sair</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>O nome da tabela a ser criada.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>O nome do campo ou campos a serem criados na nova tabela. Crie pelo menos um campo.</p></td>
</tr>
<tr class="odd">
<td><p><em>tipo</em></p></td>
<td><p>O tipo de dados do <em>campo</em> na nova tabela.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>O tamanho do campo em caracteres (somente os campos Texto e Binário).</p></td>
</tr>
<tr class="odd">
<td><p><em>índice1</em>, <em>índice2</em></p></td>
<td><p>Uma cláusula CONSTRAINT definindo um índice de campo único. Para mais informações sobre como criar esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>índicedevárioscampos</em></p></td>
<td><p>Uma cláusula CONSTRAINT definindo um índice de vários campos. Para mais informações sobre como criar esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use a instrução CREATE TABLE para definir uma nova tabela e seus campos e restrições de campo. Se NOT NULL for especificado para um campo, então será necessário que novos registros tenham dados válidos nesse campo.

Uma cláusula CONSTRAINT estabelece várias restrições sobre um campo e pode ser usada para estabelecer a chave primária. É possível também utilizar a instrução [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para criar uma chave primária ou índices extras em tabelas existentes.

Você pode usar NOT NULL em um único campo ou em uma cláusula nomeada CONSTRAINT que se aplica a um único campo ou a vários campos chamados CONSTRAINT. No entanto, você pode aplicar a restrição NOT NULL apenas uma vez a um campo. Tentar aplicar a restrição mais de uma vez acarretará um erro de tempo de execução.

Quando uma tabela TEMPORARY for criada, ela será visível somente na sessão em que for criada. Ela será excluída automaticamente quando a sessão for encerrada. As tabelas temporárias podem ser acessadas por mais de um usuário.

O atributo WITH COMPRESSION pode ser usado somente com os tipos de dados CHARACTER e MEMO (também conhecidos como TEXT) e seus sinônimos.

O atributo WITH COMPRESSION foi adicionado para as colunas de CHARACTER devido à alteração para o formato de representação de caracteres Unicode. Os caracteres Unicode exigem uniformemente dois bytes para cada caractere. Para os bancos de dados existentes do Microsoft Jet que contêm predominantemente dados de caracteres, isso pode significar que o arquivo de banco de dados poderá dobrar de tamanho quando for convertido para o formato do mecanismo de banco de dados do Microsoft Access. No entanto, a representação Unicode de vários conjuntos de caracteres, aqueles anteriormente indicados como Conjuntos de Caracteres de um Byte (SBCS), poderá ser facilmente compactada para um único byte. Se você definir uma coluna CHARACTER com esse atributo, os dados serão compactados automaticamente ao serem armazenados e descompactados quando recuperados da coluna.

As colunas MEMO também podem ser definidas para armazenar dados em um formato compactado. No entanto, há uma limitação. Somente as instâncias de colunas MEMO, quando compactadas, caberão em 4096 bytes ou menos, serão compactadas. Todas as instâncias de colunas MEMO permanecerão descompactadas. Isso significa que em uma determinada tabela, para uma determinada coluna MEMO, alguns dados poderão ser compactados e alguns dados poderão não ser compactados.

## <a name="example"></a>Exemplo

Este exemplo cria uma nova tabela chamada ThisTable com dois campos de texto.

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

Este exemplo cria uma nova tabela chamada Mytable com dois campos de texto, um campo Data/Hora e um índice exclusivo composto por todos os três campos.

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

Este exemplo cria uma nova tabela com dois campos de texto e um campo **Inteiro**.O campo CPF é a chave primária.

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

Este exemplo cria uma nova tabela chamada de `~~Kitsch'n Sync`, que demonstra todos os diferentes tipos de campo e índice. O campo Numeração Automática é a chave primária.

```vb
    Sub CreateTableX6()
        On Error Resume Next
        Application.CurrentDb.Execute "Drop Table [~~Kitsch'n Sync];"
        On Error GoTo 0
        
        'This example uses ADODB instead of the DAO shown in the previous
        'ones because DAO does not support the DECIMAL and GUID data types
        Dim con As ADODB.Connection
        Set con = CurrentProject.Connection
        con.Execute "" _
            & "CREATE TABLE [~~Kitsch'n Sync](" _
                & " [Auto]                  COUNTER" _
                & ",[Byte]                  BYTE" _
                & ",[Integer]               SMALLINT" _
                & ",[Long]                  INTEGER" _
                & ",[Single]                REAL" _
                & ",[Double]                FLOAT" _
                & ",[Decimal]               DECIMAL(18,5)" _
                & ",[Currency]              MONEY" _
                & ",[ShortText]             CHAR" _
                & ",[LongText]              MEMO" _
                & ",[PlaceHolder1]          MEMO" _
                & ",[DateTime]              DATETIME" _
                & ",[YesNo]                 BIT" _
                & ",[OleObject]             IMAGE" _
                & ",[ReplicationID]         UNIQUEIDENTIFIER" _
                & ",[Required]              INTEGER NOT NULL" _
                & ",[Unicode Compression]   MEMO WITH COMP" _
                & ",[Indexed]               INTEGER" _
                & ",CONSTRAINT [PrimaryKey] PRIMARY KEY ([Auto])" _
                & ",CONSTRAINT [Unique Index] UNIQUE ([Byte],[Integer],[Long])" _
            & ");"
        con.Execute "CREATE INDEX [Single-Field Index] ON [~~Kitsch'n Sync]([Indexed]);"
        con.Execute "CREATE INDEX [Multi-Field Index] ON [~~Kitsch'n Sync]([Auto],[Required]);"
        con.Execute "CREATE INDEX [IgnoreNulls Index] ON [~~Kitsch'n Sync]([Single],[Double]) WITH IGNORE NULL;"
        con.Execute "CREATE UNIQUE INDEX [Combined Index] ON [~~Kitsch'n Sync]([ShortText],[LongText]) WITH IGNORE NULL;"
        Set con = Nothing
    
        'Add a Hyperlink Field
        Dim AllDefs As DAO.TableDefs, TblDef As DAO.TableDef, Fld As DAO.Field
        Set AllDefs = Application.CurrentDb.TableDefs
        Set TblDef = AllDefs("~~Kitsch'n Sync")
        Set Fld = TblDef.CreateField("Hyperlink", dbMemo)
        Fld.Attributes = dbHyperlinkField + dbVariableField
        Fld.OrdinalPosition = 10
        TblDef.Fields.Append Fld
        
        DoCmd.RunSQL "ALTER TABLE [~~Kitsch'n Sync] DROP COLUMN [PlaceHolder1];"
    End Sub
```
