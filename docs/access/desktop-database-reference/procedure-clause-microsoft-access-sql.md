---
title: Cláusula PROCEDURE (Microsoft Access SQL)
TOCTitle: PROCEDURE clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dd99fb241572f2e16eae914ba7d1dea31e1d097f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924257"
---
# <a name="procedure-clause-microsoft-access-sql"></a>Cláusula PROCEDURE (Microsoft Access SQL)

**Aplica-se a**: Access 2013, o Office 2013

Define um nome e os parâmetros opcionais para uma consulta.

> [!NOTE]
> [!OBSERVAçãO] A cláusula PROCEDURE foi substituída pela instrução PROCEDURE. Embora a cláusula PROCEDURE ainda seja aceita, a instrução PROCEDURE fornece um superconjunto de recursos da cláusula PROCEDURE e é a sintaxe recomendada.

## <a name="syntax"></a>Sintaxe

O *nome* do procedimento \[ *param1 datatype*\[, *param2 datatype*\[,...\]\]

A cláusula PROCEDURE contém estas partes:

|Parte |Descrição |
|:----|:-----------|
|*name* |Um nome para o procedimento. Ele deve seguir as convenções de nomenclatura padrão.|
|*param1*, *param2* |Um ou mais campos ou parâmetros de campo. Por exemplo:
<br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Para obter mais informações sobre parâmetros, consulte [parameters](parameters-declaration-microsoft-access-sql.md).|
|*tipo de dados* | Um dos principais [tipos de dados do Microsoft Access SQL](sql-data-types.md) ou seus sinônimos. |


## <a name="remarks"></a>Comentários

Um procedimento SQL consiste em uma cláusula PROCEDURE (que especifica o nome do procedimento), uma lista opcional das definições de parâmetro e uma única instrução SQL. Por exemplo, o procedimento Get\_Part\_número pode executar uma consulta que recupera um número de peça especificado.

> [!NOTE]
> - Se a cláusula incluir mais de uma definição de campo (isto é, pares de *param-datatype* ), separe-os com vírgulas.
> - A cláusula PROCEDURE deve ser seguida por uma instrução SQL (por exemplo, uma instrução [SELECT](select-statement-microsoft-access-sql.md) ou [UPDATE](update-statement-microsoft-access-sql.md)).

## <a name="example"></a>Exemplo

Este exemplo chama a consulta CategoryList e chama o procedimento EnumFields, que pode ser encontrado no exemplo da instrução SELECT.

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
