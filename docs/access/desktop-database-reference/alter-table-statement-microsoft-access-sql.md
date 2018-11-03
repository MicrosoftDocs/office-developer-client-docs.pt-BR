---
title: Instrução ALTER TABLE (Microsoft Access SQL)
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8481102d587480577c0ba73d2da46385359a92c6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937334"
---
# <a name="alter-table-statement-microsoft-access-sql"></a>Instrução ALTER TABLE (Microsoft Access SQL)

**Aplica-se a**: Access 2013, o Office 2013

Modifica o design de uma tabela depois de ter sido criada com a instrução [CREATE TABLE](create-table-statement-microsoft-access-sql.md).

> [!NOTE]
> [!OBSERVAçãO] O mecanismo de banco de dados do Microsoft Access não oferece suporte para o uso da instrução ALTER TABLE, ou para quaisquer instruções da linguagem de definição de dados (DDL), com bancos de dados que não sejam do Microsoft Access. Use os métodos DAO **criar** .

## <a name="syntax"></a>Sintaxe

ALTER TABLE *tabela* {adicionar { *tipo de campo*de coluna\[(*tamanho*)\] \[NOT NULL\] \[restrição *índice* \] | ALTER COLUMN *tipo de campo*\[(*tamanho*)\] | RESTRIÇÃO *multifieldindex*} | DROP {coluna *campo* eu restrição *indexname*}}

A instrução ALTER TABLE possui as seguintes partes:

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
<td><p>O nome da tabela a ser alterada.</p></td>
</tr>
<tr class="even">
<td><p><em>campo</em></p></td>
<td><p>O nome do campo a ser adicionado ou excluído da <em>tabela</em>. Ou o nome do campo a ser alterado na <em>tabela</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>O tipo de dados do <em>campo</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>tamanho</em></p></td>
<td><p>O tamanho do campo em caracteres (somente os campos Texto e Binário).</p></td>
</tr>
<tr class="odd">
<td><p><em>índice</em></p></td>
<td><p>O índice de <em>campo</em>. Para obter mais informações sobre como construir esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">cláusula CONSTRAINT</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>índicecomváriasids</em></p></td>
<td><p>A definição de um índice de vários campos a serem adicionados à <em>tabela</em>. Para obter mais informações sobre como construir esse índice, consulte <a href="constraint-clause-microsoft-access-sql.md">cláusula CONSTRAINT</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>nomedoíndice</em></p></td>
<td><p>O nome do índice de vários campos a ser removido.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Usando a instrução ALTER TABLE, você pode alterar uma tabela existente de várias maneiras. É possível:

- Usar ADD COLUMN para adicionar um novo campo à tabela. Você especifica o nome do campo, o tipo de dados e (para os campos Texto e Binário) um tamanho opcional. Por exemplo, a seguinte instrução adiciona um campo Texto de 25 caracteres chamado Anotações à tabela Funcionários:
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  Você também pode definir um índice nesse campo. Para obter mais informações sobre os índices de campo único, consulte [cláusula CONSTRAINT](constraint-clause-microsoft-access-sql.md).
    
  Se você especificar NOT NULL para um campo, novos registros deverão ter dados válidos nesse campo.

- Use ALTER COLUMN para alterar o tipo de dados de um campo existente. Você especifica o nome do campo, o novo tipo de dados e um tamanho opcional para os campos Texto e Binário. Por exemplo, a seguinte instrução altera o tipo de dados de um campo chamado CEP na tabela Funcionários (originalmente definido como Inteiro) para um campo Texto de 10 caracteres:
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- Use ADD CONSTRAINT para adicionar um índice de vários campos. Para obter mais informações sobre os índices de vários campos, consulte [cláusula CONSTRAINT](constraint-clause-microsoft-access-sql.md).

- Use DROP COLUMN para excluir um campo. Você especifica somente o nome do campo.

- Use DROP CONSTRAINT para excluir um índice de vários campos. Você especifica somente o nome do índice que segue a palavra reservada CONSTRAINT.


> [!NOTE] 
> - [!OBSERVAçãO] Não é possível adicionar ou excluir mais de um campo ou índice por vez.
> - Você pode usar a instrução [CREATE INDEX](create-index-statement-microsoft-access-sql.md) para adicionar um índice de campo único ou de vários campos a uma tabela, e pode usar as instruções ALTER TABLE ou [DROP](drop-statement-microsoft-access-sql.md) para excluir um índice criado com ALTER TABLE ou CREATE INDEX.
> - Você pode usar NOT NULL em um campo único ou em uma cláusula nomeada CONSTRAINT que se aplica a um campo único ou a vários campos nomeados CONSTRAINT. No entanto, é possível aplicar a restrição NÃO NULO apenas uma vez em um campo. Tentar aplicar essa restrição mais de uma vez pode resultar em um erro de tempo de execução. 


## <a name="example"></a>Exemplo

Este exemplo adiciona um campo Salário com o tipo de dados **Dinheiro** à tabela Funcionários.

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Este exemplo altera o campo Salário do tipo de dados **Dinheiro** para o tipo de dados de **Caractere**.

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Este exemplo remove o campo Salário da tabela Funcionários.

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Este exemplo adiciona uma chave estrangeira à tabela Pedidos. A chave estrangeira é baseada no campo IDdoFuncionário e se refere ao campo IDdoFuncionário na tabela Funcionários. Neste exemplo, não é necessário listar o campo IDdoFuncionário depois da tabela Funcionários na cláusula REFERENCES, pois a IDdoFuncionário é a principal chave da tabela Funcionários.

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Este exemplo remove a chave estrangeira da tabela Pedidos.

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
