---
title: Instrução INSERT INTO (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 4fee5e9e8878274f2c20dd83a3dbedaf2903ca62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291330"
---
# <a name="insert-into-statement-microsoft-access-sql"></a>Instrução INSERT INTO (Microsoft Access SQL)

**Aplica-se ao:** Access 2013, Office 2013

Adiciona um registro ou vários registros a uma tabela. Isso é conhecido como uma consulta acréscimo.

## <a name="syntax"></a>Sintaxe

### <a name="multiple-record-append-query"></a>Consulta acréscimo de vários registros:

INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*

### <a name="single-record-append-query"></a>Consulta acréscimo de registro único:

INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])

A instrução INSERT INTO inclui as seguintes partes:

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
<td><p><em>target</em></p></td>
<td><p>O nome da tabela ou da consulta à qual acrescentar registros.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>Nome dos campos aos quais acrescentar dados, ao seguir um argumento <em>destino</em> ou os nomes dos campos dos quais obter dados, ao seguir um argumento <em>fonte</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>O caminho para um banco de dados externo. Para obter a descrição do caminho, consulte a cláusula <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>O nome da tabela ou da consulta da qual copiar registros.</p></td>
</tr>
<tr class="odd">
<td><p><em>tableexpression</em></p></td>
<td><p>O nome da tabela ou tabelas a partir das quais os registros são inseridos. Esse argumento poderá ser um nome de tabela única ou um composto resultante de uma operação <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> ou <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a>, ou de uma consulta salva.</p></td>
</tr>
<tr class="even">
<td><p><em>value1</em>, <em>value2</em></p></td>
<td><p>Os valores para inserir em campos específicos do novo registro. Cada valor é inserido no campo correspondente à posição do valor na lista: o <em>valor1</em> é inserido no <em>campo1</em> do novo registro, o <em>valor2</em> no <em>campo2</em> e assim por diante. É necessário separar os valores com vírgula e delimitar os campos de texto entre aspas (" ").</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você poderá utilizar a instrução INSERT INTO para adicionar registros únicos em uma tabela, usando a sintaxe da consulta acréscimo de registro único, como descrito acima. Nesse caso, seu código vai especificar o nome e o valor para cada campo do registro. Você deverá especificar os campos do registro aos quais vai atribuir um valor e especificar um valor para cada campo. Se você não especificar os campos, o valor padrão ou **Nulo** será inserido nas colunas ausentes. Os registros serão adicionados ao final da tabela.

É possível também utilizar a instrução INSERT INTO para acrescentar um conjunto de registros de outra tabela ou consulta usando as cláusulas SELECT … FROM, como descrito acima, na sintaxe de consulta acréscimo de múltiplos registros. Nesse caso, a cláusula SELECT especificar os campos para acrescentar às tabelas de *destino* indicadas.

A tabela *fonte* ou *destino* poderá especificar uma tabela ou uma consulta. Se uma consulta for especificada, o mecanismo do banco de dados do Microsoft Access acrescentará registros a todas as tabelas especificadas pela consulta.

A instrução INSERT INTO é opcional, mas se for incluída, prevalecerá sobre a [SELECT](select-statement-microsoft-access-sql.md).

Se sua tabela de destino incluir uma chave primária, acrescente somente valores não **Nulos** ao campo ou campos dessa chave; caso não o faça, o mecanismo do banco de dados do Microsoft Access não acrescentará os registros.

Se acrescentar registros a uma tabela com o campo Numeração Automática e desejar renumerá-los, não inclua esse campo à consulta. Inclua o campo Numeração Automática na consulta somente se desejar manter os valores originais desse campo.

Use a cláusula IN para acrescentar registros a uma tabela em outro banco de dados.

Para criar uma nova tabela, use as instruções [SELECT… INTO](select-into-statement-microsoft-access-sql.md), em vez de criar uma consulta Criar Tabela.

Para descobrir quais registros serão acrescentados antes de executar a consulta acréscimo, em primeiro lugar, execute e verifique os resultados de uma consulta seleção, que utiliza os mesmos critérios de seleção.

Uma consulta acréscimo copia os registros de uma ou de mais tabelas para outra. As tabelas que englobarem os registros que você anexar não serão afetadas pela consulta acréscimo.

Em vez de acrescentar registros existentes de outra tabela, é possível especificar o valor de cada campo em um novo registro único, usando a cláusula VALUES.  Se omitir a lista de campos, a cláusula VALUES deverá incluir um valor para cada campo na tabela; caso contrário, a operação INSERT vai falhar. Utilize uma instrução INSERT INTO extra com uma cláusula VALUES para cada registro adicional que desejar criar.

**Links fornecidos pela** comunidade [UtterAccess](https://www.utteraccess.com). UtterAccess é o fórum principal de wiki e ajuda do Microsoft Access.

- [Como gerar números sequenciais para as instruções INSERT/UPDATE](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [SQL para Formatador VBA](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a>Exemplo

Este exemplo seleciona todos os registros em uma tabela hipotética Novos Clientes e os adiciona à tabela Clientes. Se as colunas individuais não forem determinadas, os nomes das colunas da tabela SELECT devem corresponder exatamente àqueles na tabela INSERT INTO.

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

Esse exemplo cria um novo registro na tabela Funcionários.

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

