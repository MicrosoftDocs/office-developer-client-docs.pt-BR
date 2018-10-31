---
title: Instrução UPDATE (Microsoft Access SQL)
TOCTitle: UPDATE statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7a761fbc6404cf72818271b956bfc63516942d25
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863280"
---
# <a name="update-statement-microsoft-access-sql"></a>Instrução UPDATE (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013

Cria uma consulta de atualização que altera os valores nos campos em uma tabela especificada com base em critérios específicos.

## <a name="syntax"></a>Sintaxe

ATUALIZAÇÃO *tabela* SET *newvalue* onde *critérios*;

A instrução UPDATE contém estas partes:

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
<td><p><em>table</em></p></td>
<td><p>O nome da tabela que contém os dados que você deseja modificar.</p></td>
</tr>
<tr class="even">
<td><p><em>newvalue</em></p></td>
<td><p>Uma expressão que determina o valor a ser inserido em um determinado campo nos registros atualizados.</p></td>
</tr>
<tr class="odd">
<td><p><em>criteria</em></p></td>
<td><p>Uma expressão que determina quais registros serão atualizados. Somente os registros que atendem à expressão são atualizados.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

UPDATE é especialmente útil quando você deseja alterar muitos registros ou quando os registros que deseja alterar estão em várias tabelas.

Você pode alterar vários campos ao mesmo tempo. O exemplo a seguir aumenta os valores Total de Pedidos em 10% e os valores Frete em 3% para transportadoras no Reino Unido:

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- UPDATE não gerar um conjunto de resultados. Além disso, depois de atualizar registros utilizando uma consulta de atualização, você não poderá desfazer a operação. Se você quiser saber quais registros foram atualizados, primeiro examine os resultados de uma consulta de seleção que use os mesmos critérios e, em seguida, execute a consulta de atualização.
- Sempre faça cópias de backup dos dados. Se você atualizar registros erroneamente, será possível recuperá-los das cópias de backup.




## <a name="example"></a>Exemplo

Este exemplo altera os valores no campo Gerente para 5 em todos os registros de funcionários que têm atualmente valores 2 em  Gerente.



```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```
