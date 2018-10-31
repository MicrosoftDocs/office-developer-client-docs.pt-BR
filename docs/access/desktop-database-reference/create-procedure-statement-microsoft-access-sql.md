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
ms.openlocfilehash: 573ec86a573697ebe52886535f8544bbaab61d7d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861460"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>Instrução CREATE PROCEDURE (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013 

Cria um procedimento armazenado.

> [!NOTE]
> [!OBSERVAçãO] O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE PROCEDURE nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Jet.

## <a name="syntax"></a>Sintaxe

CREATE PROCEDURE *procedimento* \[ *param1 datatype*\[, *param2 datatype*\[,... \] \] Como sqlstatement

A instrução PROCEDURE INDEX contém estas partes:

|Parte|Descrição|
|:---|:----------|
|*procedimento*|Um nome para o procedimento. Ele deve seguir as convenções de nomenclatura padrão.|
|*param1*, *param2*|De 1 a 255 nomes de campo ou parâmetros. Por exemplo:
<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Para obter mais informações sobre parâmetros, consulte [PARAMETERS](parameters-declaration-microsoft-access-sql.md).|
|*tipo de dados*|Um dos principais [tipos de dados do Microsoft Access SQL](sql-data-types.md) ou seus sinônimos.|
|*sqlstatement*|Uma instrução SQL como SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE e assim por diante.|


## <a name="remarks"></a>Comentários

Um procedimento SQL consiste em uma cláusula PROCEDURE que especifica o nome do procedimento, uma lista opcional de definições de parâmetros e uma instrução SQL única.

Um nome de procedimento não pode ser o mesmo de uma tabela existente.

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
