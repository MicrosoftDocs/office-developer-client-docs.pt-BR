---
title: Instrução CREATE PROCEDURE (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: f223e164bd36a6a1a76140a28dd57cd2005e4a20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295398"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>Instrução CREATE PROCEDURE (Microsoft Access SQL)

**Aplica-se ao**: Access 2013, Office 2013 

Cria um procedimento armazenado.

> [!NOTE]
> O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE PROCEDURE nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Jet.

## <a name="syntax"></a>Sintaxe

CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement

A instrução CREATE PROCEDURE tem as seguintes partes:

|Sair|Descrição|
|:---|:----------|
|*procedure*|Um nome para o procedimento. Ele deve seguir as convenções de nomenclatura padrão.|
|*param1*, *param2*|De um a 255 nomes ou parâmetros de campo. Por exemplo:<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Para obter mais informações sobre parâmetros, consulte [PARAMETERS](parameters-declaration-microsoft-access-sql.md).|
|*datatype*|Um dos principais [tipos de dados do Microsoft Access SQL](sql-data-types.md) ou seus sinônimos.|
|*sqlstatement*|Uma instrução SQL, como SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE e assim por diante.|


## <a name="remarks"></a>Comentários

Um procedimento SQL consiste em uma instrução PROCEDURE que especifica o nome do procedimento, uma lista opcional de definições de parâmetros e uma única instrução SQL.

O nome de um procedimento não pode ser igual ao nome de uma tabela existente.

## <a name="example"></a>Exemplo

Este exemplo chama a consulta CategoryList e o procedimento EnumFields, o que pode ser localizado no exemplo da instrução SELECT.

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
