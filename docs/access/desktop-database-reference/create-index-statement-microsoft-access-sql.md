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
# <a name="create-index-statement-microsoft-access-sql"></a>Instrução CREATE INDEX (Microsoft Access SQL)

**Aplica-se ao**: Access 2013, Office 2013

Cria um novo índice em uma tabela existente.

> [!NOTE]
> Para bancos de dados de mecanismo de banco de dados não Microsoft Access, o mecanismo de banco de dados Microsoft Access não fornece suporte ao uso de CREATE INDEX (exceto para criar um pseudo índice em uma tabela ODBC vinculada) nem de nenhuma instrução de linguagem de definição de dados (DDL). Em vez disso, utilize os métodos DAO **Criar**. Para mais informações, consulte a seção Comentários.

## <a name="syntax"></a>Sintaxe

CREATE \[ UNIQUE \] INDEX *índice* ON *tabela* (*campo* \[ASC|DESC\]\[, *campo* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]

A instrução CREATE INDEX tem as seguintes partes:

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
<td><p><em>índice</em></p></td>
<td><p>O nome do índice a ser criado.</p></td>
</tr>
<tr class="even">
<td><p><em>tabela</em></p></td>
<td><p>O nome da tabela existente que conterá o índice.</p></td>
</tr>
<tr class="odd">
<td><p><em>campo</em></p></td>
<td><p>O nome do(s) campo(s) a ser indexado. Para criar um índice de campo único, liste o nome do campo entre parênteses, após o nome da tabela. Para criar um índice de vários campos, liste o nome de cada campo a ser incluído no índice. Para criar índices em ordem decrescente, use a palavra reservada DESC; caso contrário, os índices serão considerados como crescente.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Para proibir valores duplicados nos campos indexados de registros diferentes, use a palavra reservada UNIQUE.

Na cláusula opcional WITH, você pode aplicar regras de validação de dados. Você pode:

- Proibir entradas nulas nos campos indexados de novos registros, usando a opção DISALLOW NULL.

- Impedir que registros com valores **Null** nos campos indexados sejam incluídos no índice, usando a opção IGNORE NULL.

- Designar o campo ou os campos indexados como a chave primária, utilizando a palavra reservada PRIMARY. Isso implica que a chave seja exclusiva, para que você possa omitir a palavra reservada UNIQUE.

Você pode usar CREATE INDEX para criar um pseudo índice em uma tabela vinculada em uma fonte de dados ODBC, como o Microsoft SQL Server, que ainda não tem um índice. Não é necessário ter permissão ou acesso ao servidor remoto para criar um pseudoíndice, e o banco de dados remoto reconhece a presença do pseudoíndice e não é afetado por ele. Use a mesma sintaxe para tabelas vinculadas e nativas. Pode ser especialmente útil criar um pseudoíndice em uma tabela que normalmente seria somente leitura.

Também é possível usar a instrução [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para adicionar um índice de único arquivo ou de vários arquivos a uma tabela, e a instrução ALTER TABLE ou [DROP](drop-statement-microsoft-access-sql.md) para remover um índice criado com ALTER TABLE ou CREATE INDEX.

> [!NOTE]
> Não use a palavra reservada PRIMARY ao criar um novo índice em uma tabela que já tem uma chave primária; se você fizer isso, ocorrerá um erro.

## <a name="example"></a>Exemplo

Este exemplo cria um índice que consiste nos campos Telefone Residencial e Ramal na tabela Funcionários.

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

Este exemplo cria um índice na tabela Customers utilizando o campo CustomerID. Dois registros não podem ter os mesmos dados no campo CustomerID e nenhum valor nulo é permitido.

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
