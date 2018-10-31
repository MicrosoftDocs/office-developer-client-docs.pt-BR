---
title: Cláusula CONSTRAINT (Microsoft Access SQL)
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
ms.openlocfilehash: 87870d824f9e26f601529bc60b737f1e46b12960
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863000"
---
# <a name="constraint-clause-microsoft-access-sql"></a>Cláusula CONSTRAINT (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013

Uma restrição é semelhante a um índice, embora possa ser usada para estabelecer uma relação com outra tabela.

Use a cláusula CONSTRAINT em instruções [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) e [CREATE TABLE](create-table-statement-microsoft-access-sql.md) para criar ou excluir restrições. Existem dois tipos de cláusula CONSTRAINT: uma para criação de uma restrição em um campo único e outra para criação de mais de um campo.

> [!NOTE]
> [!OBSERVAçãO] O mecanismo de banco de dados do Microsoft Access não suporta o uso de CONSTRAINT ou de nenhuma das instruções DDL (Data Definition Language) com bancos de dados do mecanismo de bancos de dados de terceiros. Use os métodos DAO **criar** .

## <a name="syntax"></a>Sintaxe

**Restrição de campo único**:

O *nome* da restrição {chave primária | EXCLUSIVO | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | Definir NULL\] \[ON DELETE CASCADE | Definir NULL\]}

**Restrição de vários campos**:

O *nome* da restrição {chave primária (*primary1*\[, *primary2* \[,... \]\]) | EXCLUSIVO (*unique1*\[, *unique2* \[,... \]\]) | NOT NULL (*notnull1*\[, *notnull2* \[,... \]\]) | CHAVE estrangeira \[nenhum índice\] (*ref1*\[, *ref2* \[,... \] \]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[,... \] \])\] \[ON UPDATE CASCADE | Definir NULL\] \[ON DELETE CASCADE | Definir NULL\]}

A cláusula CONSTRAINT possui as seguintes partes:

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
<td><p><em>name</em></p></td>
<td><p>O nome da restrição que será criada.</p></td>
</tr>
<tr class="even">
<td><p><em>primary1</em>, <em>primary2</em></p></td>
<td><p>O nome do campo ou dos campos que será designado como a chave primária.</p></td>
</tr>
<tr class="odd">
<td><p><em>unique1</em>, <em>unique2</em></p></td>
<td><p>O nome do campo ou dos campos que será designado como uma chave exclusiva.</p></td>
</tr>
<tr class="even">
<td><p><em>notnull1, notnull2</em></p></td>
<td><p>O nome do campo ou dos campos restrito a valores não-nulos.</p></td>
</tr>
<tr class="odd">
<td><p><em>ref1</em>, <em>ref2</em></p></td>
<td><p>O nome de um campo ou campos de chave estrangeira que se refere a campos em outra tabela.</p></td>
</tr>
<tr class="even">
<td><p><em>foreigntable</em></p></td>
<td><p>O nome da tabela externa que contém o campo ou os campos especificado por <em>foreignfield</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>foreignfield1</em>, <em>foreignfield2</em></p></td>
<td><p>O nome do campo ou dos campos em <em>foreigntable</em> especificados por <em>ref1</em>, <em>ref2</em>. Omita essa cláusula se o campo referido for a chave primária de <em>foreigntable</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use a sintaxe de restrição de campo único na cláusula de definição de campo de uma instrução ALTER TABLE ou CREATE TABLE imediatamente depois da especificação do tipo de dados de campo.

Use a sintaxe de restrição de vários campos sempre que usar a palavra reservada CONSTRAINT fora da cláusula de definição de campo em uma instrução de ALTER TABLE ou CREATE TABLE.

Pelo uso de CONSTRAINT, você pode designar um campo como um dos seguintes tipos de restrições:

- Use a palavra reservada UNIQUE para designar um campo como uma chave exclusiva. Isso significa que nenhum dos dois registros na tabela pode ter o mesmo valor nesse campo. Você pode restringir qualquer campo ou lista de campos como exclusivo. Se uma restrição de vários campos for designada como uma chave exclusiva, os valores combinados de todos os campos no índice devem ser exclusivos, mesmo se dois ou mais registros tiverem o mesmo valor em apenas um dos campos.

- Use as palavras reservadas PRIMARY KEY para designar um campo ou conjunto de campos em uma tabela como uma chave primária. Todos os valores na chave primária devem ser exclusivos e não **Nulos** e pode existir somente uma chave primária para uma tabela.
    
  > [!NOTE]
  > [!OBSERVAçãO] Não defina uma restrição PRIMARY KEY em uma tabela que já tenha uma chave primária; isso pode ocasionar um erro.

- Use as palavras reservadas FOREIGN KEY para designar um campo como uma chave estrangeira. Se a chave primária da tabela externa for composta de mais de um campo, use uma definição de restrição de campo múltiplo, listando todos os campos de referência, o nome da tabela externa e os nomes dos campos referenciados na tabela externa, na mesma ordem em que estão listados os campos de referência. Se o campo ou os campos de referência forem a chave primária da tabela externa, não será necessário especificar os campos referenciados. Por padrão, o mecanismo de banco de dados se comporta como se a chave primária da tabela externa fosse os campos referenciados. As restrições da chave estrangeira definem ações específicas que serão executadas quando for alterado um valor de chave primária correspondente:

- Você pode especificar as ações que serão executadas na tabela externa baseada em uma ação correspondente executada em uma chave primária na tabela em que CONSTRAINT está definida. Por exemplo, considere a seguinte definição da tabela Customers:
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Considere a seguinte definição da tabela Orders, que define a relação da chave estrangeira ao fazer referência à chave primária da tabela Customers:
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  Ambas as cláusulas ON UPDATE CASCADE e ON DELETE CASCADE estão definidas na chave estrangeira. A cláusula ON UPDATE CASCADE significa que, se um identificador de cliente (CustId) for atualizado na tabela Customer, a atualização será feita em cascata na tabela Orders. Cada pedido que tiver um valor identificador de cliente correspondente será atualizado automaticamente com o novo valor. A cláusula ON DELETE CASCADE significa que, se um cliente for excluído da tabela Customer, todas as linhas da tabela Orders que contenham o mesmo valor identificador de cliente também serão excluídas. Considere as seguintes definições diferentes da tabela Orders, usando a ação SET NULL em vez da ação CASCADE:
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  A cláusula ON UPDATE SET NULL significa que, se um identificador de cliente (CustId) for atualizado na tabela Customer, os valores da chave estrangeira correspondentes na tabela Orders serão automaticamente definidos como NULL. De forma semelhante, a cláusula ON DELETE SET NULL significa que, se um cliente for excluído da tabela Customer, todas as chaves estrangeiras correspondentes na tabela Orders serão definidas automaticamente como NULL.

Para impedir a criação automática de índices das chaves estrangeiras, use o modificador NO INDEX. Essa forma de definição da chave estrangeira deve ser usada somente nos casos em que os valores de índice resultantes forem duplicados com frequência. Quando os valores de um índice de chave estrangeira forem duplicados com frequência, o uso de um índice pode ser menos eficiente do que simplesmente examinar a tabela. A manutenção desse tipo de índice com linhas inseridas e excluídas da tabela, prejudica o desempenho e não traz nenhum benefício.

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

