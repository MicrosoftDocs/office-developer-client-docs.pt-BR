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
# <a name="create-table-statement-microsoft-access-sql"></a>Instrução CREATE TABLE (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013

Cria uma nova tabela.

> [!NOTE]
> [!OBSERVAçãO] O mecanismo do banco de dados do Microsoft Access não suporta o uso da instrução CREATE TABLE ou de quaisquer das instruções DDL com mecanismos de bancos de dados que não sejam do Microsoft Access. Em vez disso, use os métodos Create DAO.

## <a name="syntax"></a>Sintaxe

CRIAR \[temporário\] tabela *tabela* (*tipo field1* \[(*tamanho*)\] \[NOT NULL\] \[WITH COMPRESSION | COM COMPOSIÇÃO\] \[ *index1* \] \[, *field2* *tipo* \[(*tamanho*)\] \[NOT NULL\] \[ *índice 2* \] \[,... \] \] \[, Restrição *multifieldindex* \[,... \]\])

A instrução CREATE TABLE contém as seguintes partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>tabela</em></p></td>
<td><p>O nome da tabela a ser criado.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>O nome do campo ou dos campos a serem criados na nova tabela. É necessário criar pelo menos um campo.</p></td>
</tr>
<tr class="odd">
<td><p><em>tipo</em></p></td>
<td><p>O tipo de dados do <em>campo</em> na nova tabela.</p></td>
</tr>
<tr class="even">
<td><p><em>tamanho</em></p></td>
<td><p>O tamanho do campo em caracteres (somente campos de texto e campos binários).</p></td>
</tr>
<tr class="odd">
<td><p><em>índice1</em>, <em>índice2</em></p></td>
<td><p>Uma cláusula CONSTRAINT definindo um índice de campo único. Para obter mais informações sobre como criar esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.  </p></td>
</tr>
<tr class="even">
<td><p><em>índicecomváriasids</em></p></td>
<td><p>Uma cláusula CONSTRAINT definindo um índice de campos múltiplos. Para obter mais informações sobre como criar esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">Cláusula CONSTRAINT</a>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Utilize a instrução CREATE TABLE para definir uma nova tabela e seus campos, além das restrições de campo. Se for especificado NOT NULL para um campo, então será necessário que os novos registros tenham dados válidos nesse campo.

Uma cláusula CONSTRAINT estabelece várias restrições sobre um campo e pode ser usada para estabelecer a chave primária. É possível também utilizar a instrução [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para criar uma chave primária ou índices extras em tabelas existentes.

Você poderá usar NOT NULL em um campo único ou dentro de uma cláusula CONSTRAINT nomeada, que se aplica a um campo único ou a um campo múltiplo. No entanto, é possível aplicar a restrição NOT NULL a um campo somente uma vez. A tentativa de aplicar esta restrição mais de uma vez resultará em um erro em tempo de execução.

Quando uma tabela temporária for criada, ela será visível somente na sessão em que for criada. Ela será excluída automaticamente, ao encerrar a sessão. Essas tabelas podem ser acessadas por mais de um usuário.

O atributo WITH COMPRESSION pode ser utilizado com os tipos de dados Caractere e Memorando (também conhecido como Texto) e seus sinônimos.

O atributo WITH COMPRESSION foi adicionado às colunas Caracteres por causa da alteração para o formato de representação de caracteres Unicode. Os caracteres Unicode exigem dois bytes uniformemente para cada caractere. Para os bancos de dados existentes do Microsoft® Jet, que contêm predominantemente dados de caracteres, isso pode significar que o arquivo de banco de dados poderá dobrar de tamanho quando for convertido para o formato do mecanismo de banco de dados do Microsoft Access. No entanto, a representação Unicode de vários conjuntos de caracteres, aqueles anteriormente indicados como conjuntos de caracteres de um byte (SBCS), poderá ser facilmente compactada para um único byte. Se definir uma coluna Caractere com esse atributo, os dados serão automaticamente compactados, à medida que forem armazenados e descompactados, ao serem resgatados de uma coluna.

As colunas Memorando também podem ser definidas para armazenar dados em formato compactado. No entanto, existe uma limitação. Somente as instâncias de colunas Memorando que tiverem 4096 bytes ou menos serão compactadas. Todas as outras instâncias de colunas Memorando permanecerão descompactadas. Isso significa que, dentro de uma determinada tabela, para uma determinada coluna Memorando, alguns dados podem ser compactados e outros não.

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
