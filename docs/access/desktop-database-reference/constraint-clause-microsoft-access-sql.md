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
# <a name="constraint-clause-microsoft-access-sql"></a>Cláusula de RESTRIÇÃO (Microsoft Access SQL)

**Aplica-se ao**: Access 2013, Office 2013

Uma restrição é semelhante a um índice, embora possa ser usada para estabelecer uma relação com outra tabela.

Use a cláusula CONSTRAINT em instruções [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) e [CREATE TABLE](create-table-statement-microsoft-access-sql.md) para criar ou excluir restrições. Existem dois tipos de cláusula CONSTRAINT: uma para criação de uma restrição em um campo único e outra para criação de mais de um campo.

> [!NOTE]
> O mecanismo de banco de dados do Microsoft Access não suporta o uso de CONSTRAINT ou de nenhuma das instruções DDL (Data Definition Language) com bancos de dados do mecanismo de bancos de dados de terceiros. Em vez disso, utilize os métodos DAO **Criar**.

## <a name="syntax"></a>Sintaxe

### <a name="single-field-constraint"></a>Restrição de campo único:

RESTRIÇÃO*nome* {CHAVE PRIMÁRIA | EXCLUSIVA | NÃO NULO | REFERÊNCIAS *tabelaestrangeira* \[(*campoestrangeiro1, campoestrangeiro2*)\] \[A ATUALIZAR CASCATA | DEFINIR NULO \] \[A DELETAR CASCATA | DEFINIR NULO \]}

### <a name="multiple-field-constraint"></a>Restrição de vários campos:

RESTRIÇÃO*nome* {CHAVE PRIMÁRIA (*primária1*\[, *primária2* \[, …\]\]) | EXCLUSIVA (*exclusiva1*\[, *exclusiva2* \[, …\]\]) | NÃO NULO (*nãonulo1*\[, *nãonulo2* \[, …\]\]) | CHAVE ESTRANGEIRA \[NENHUM ÍNDICE\] (*ref1*\[, *ref2* \[, …\]\]) REFERÊNCIAS *tabelaestrangeira* \[(*campoestrangeiro1* \[, *campoestrangeiro2* \[, …\]\])\] \[A ATUALIZAR CASCATA | DEFINIR NULO\] \[A DELETAR CASCATA | DEFINIR NULO\]}

A cláusula CONSTRAINT tem as seguintes partes:

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
<td><p><em>name</em></p></td>
<td><p>O nome da restrição a ser criada.</p></td>
</tr>
<tr class="even">
<td><p><em>primária1</em>, <em>primária2</em></p></td>
<td><p>O nome do campo ou dos campos que será designado como a chave primária.</p></td>
</tr>
<tr class="odd">
<td><p><em>exclusiva1</em>, <em>exclusiva2</em></p></td>
<td><p>O nome dos campos que serão designados como uma chave exclusiva.</p></td>
</tr>
<tr class="even">
<td><p><em>nãonulo1, nãonulo2</em></p></td>
<td><p>O nome dos campos restritos a valores não nulos.</p></td>
</tr>
<tr class="odd">
<td><p><em>ref1</em>, <em>ref2</em></p></td>
<td><p>O nome de um campo ou campos de chave estrangeira que se refere a campos em outra tabela.</p></td>
</tr>
<tr class="even">
<td><p><em>tabelaestrangeira</em></p></td>
<td><p>O nome da tabela externa que contém o campo ou os campos especificado por <em>foreignfield</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>campoestrangeiro1</em>, <em>campoestrangeiro2</em></p></td>
<td><p>O nome dos campos em <em>tabelaestrangeira</em> especificados por <em>ref1</em>, <em>ref2</em>. Você poderá omitir essa cláusula se o campo de referência for a chave primária de <em>tabelaestrangeira</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use a sintaxe para uma restrição de campo único na cláusula de definição de campo de uma instrução ALTER TABLE ou CREATE TABLE, imediatamente após a especificação do tipo de dado do campo.

Use a sintaxe de restrição de vários campos sempre que usar a palavra reservada CONSTRAINT fora da cláusula de definição de campo em uma instrução de ALTER TABLE ou CREATE TABLE.

Com CONSTRAINT, você pode designar um campo como um dos seguintes tipos de restrições:

- Você pode usar a palavra reservada UNIQUE para designar um campo como uma chave exclusiva. Isso significa que nenhum registro da tabela terá o mesmo valor nesse campo. Você pode restringir qualquer campo ou lista de campos como exclusivo. Se uma restrição de campos múltiplos for designada como uma chave exclusiva, os valores combinados de todos os campos no índice deverão ser exclusivos, mesmo que dois ou mais registros tenham o mesmo valor em apenas um dos campos.

- Você pode usar as palavras reservadas PRIMARY KEY para designar um campo ou um conjunto de campos em uma tabela como chave primária. Todos os valores de chave primária devem ser exclusivos e não **nulos**, e pode haver apenas uma chave primária em uma tabela.
    
  > [!NOTE]
  > Não defina uma restrição PRIMARY KEY em uma tabela que já tem uma chave primária; se você fizer isso, ocorrerá um erro.

- Use as palavras reservadas FOREIGN KEY para designar um campo como uma chave estrangeira. Se a chave primária da tabela externa for composta de mais de um campo, use uma definição de restrição de campo múltiplo, listando todos os campos de referência, o nome da tabela externa e os nomes dos campos referenciados na tabela externa, na mesma ordem em que estão listados os campos de referência. Se o campo ou os campos de referência forem a chave primária da tabela externa, não será necessário especificar os campos referenciados. Por padrão, o mecanismo de banco de dados se comporta como se a chave primária da tabela externa fosse os campos referenciados. As restrições da chave estrangeira definem ações específicas que serão executadas quando for alterado um valor de chave primária correspondente:

- É possível especificar as ações a serem executadas na tabela estrangeira com base em uma ação correspondente realizada em uma chave primária na tabela em que CONSTRAINT é definida. Por exemplo, considere a seguinte definição da tabela Customers (Clientes):
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Considere a seguinte definição da tabela Orders (Pedidos), que define uma relação de chave estrangeira que faz referência à chave primária da tabela Customers:
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  Ambas as cláusulas ON UPDATE CASCADE e ON DELETE CASCADE estão definidas na chave estrangeira. A cláusula ON UPDATE CASCADE significa que, se um identificador de cliente (CustId) for atualizado na tabela Customer, a atualização será feita em cascata na tabela Orders. Cada pedido que tiver um valor identificador de cliente correspondente será atualizado automaticamente com o novo valor. A cláusula ON DELETE CASCADE significa que, se um cliente for excluído da tabela Customer, todas as linhas da tabela Orders que contenham o mesmo valor identificador de cliente também serão excluídas. Considere as seguintes definições diferentes da tabela Orders, usando a ação SET NULL em vez da ação CASCADE:
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  A cláusula ON UPDATE SET NULL significa que, se o identificador do cliente (CustId) for atualizado na tabela Customer, os valores de chave estrangeira correspondentes na tabela Orders serão definidos automaticamente como NULL. Da mesma forma, a cláusula ON DELETE SET NULL significa que, se um cliente for excluído na tabela Customer, todas as chaves estrangeiras correspondentes na tabela Orders serão definidas automaticamente como NULL.

Para impedir a criação automática de índices para chaves estrangeiras, é possível usar o modificador NO INDEX. Essa forma de definição de chave estrangeira deve ser usada somente em casos em que os valores de índice resultantes seriam duplicados com frequência. Nos casos em que os valores de um índice de chave estrangeira são duplicados com frequência, o uso de um índice pode ser menos eficaz do que simplesmente executar uma verificação de tabela. Manter esse tipo de índice, com linhas inseridas e excluídas da tabela, reduz o desempenho e não oferece benefícios.

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

