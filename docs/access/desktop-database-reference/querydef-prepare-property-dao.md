---
title: Propriedade QueryDef.Prepare (DAO)
TOCTitle: Prepare Property
ms:assetid: d5a285c4-bd00-028b-b785-f1890db29bab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835035(v=office.15)
ms:contentKeyID: 48547968
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101187
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ac05510a218d1cf4cf925acc2ca8908b7bcbcd03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303266"
---
# <a name="querydefprepare-property-dao"></a>Propriedade QueryDef.Prepare (DAO)

**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . Preparar

*expressão* Uma variável que representa um objeto **QueryDef**.

## <a name="remarks"></a>Comentários

Use a propriedade **Prepare** para que o servidor crie um procedimento armazenado temporariamente da consulta e depois execute-o ou apenas execute a consulta diretamente. Por padrão, a propriedade **Prepare** está definida como **dbQPrepare**. No entanto, é possível definir essa propriedade como **dbQUnprepare** para proibir a preparação da consulta. Nesse caso, a consulta será executa pela API **SQLExecDirect**.

A criação de um procedimento armazenado pode reduzir a velocidade da operação inicial, mas aumenta o desempenho de todas as referências subsequentes da consulta. No entanto, algumas consultas não podem ser executadas no formulário de procedimentos armazenados. Nesses casos, defina a propriedade **Prepare** como **dbQUnprepare**.

Se **Preparar** estiver definido como **dbQPrepare,** isso poderá ser substituído quando a consulta for executada definindo o argumento de opções do método **[Execute](querydef-execute-method-dao.md)** como **dbExecDirect**.

> [!NOTE]
> [!OBSERVAçãO] A API **SQLPrepare** do ODBC será chamada assim que a propriedade **[SQL](querydef-sql-property-dao.md)** do DAO for definida. Por esse motivo, se você deseja melhorar o desempenho usando a opção **dbQUnprepare**, deverá definir a propriedade **Prepare** antes de definir a propriedade **SQL**.

## <a name="example"></a>Exemplo

Este exemplo usa propriedade **Prepare** para especificar que a consulta deverá ser executada diretamente em vez de criar primeiro um procedimento temporário armazenado no servidor.

```vb 
Sub PrepareX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set qdfTemp = conPubs.CreateQueryDef("") 
 
 With qdfTemp 
 ' Because you will only run this query once, specify 
 ' the ODBC SQLExecDirect API function. If you do 
 ' not set this property before you set the SQL 
 ' property, the ODBC SQLPrepare API function will 
 ' be called anyway which will nullify any 
 ' performance gain. 
 .Prepare = dbQUnprepare 
 .SQL = "UPDATE roysched " & _ 
 "SET royalty = royalty * 2 " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'" 
 .Execute 
 End With 
 
 Debug.Print "Query results:" 
 
 ' Open recordset containing modified records. 
 Set rstTemp = conPubs.OpenRecordset( _ 
 "SELECT * FROM roysched " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'") 
 
 ' Enumerate recordset. 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , !title_id, !lorange, _ 
 !hirange, !royalty 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 conPubs.Close 
 wrkODBC.Close 
 
```

