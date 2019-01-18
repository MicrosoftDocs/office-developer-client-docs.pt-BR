---
title: Propriedade QueryDef.MaxRecords (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6738762ba18289293c67392d47e278066ead071d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699307"
---
# <a name="querydefmaxrecords-property-dao"></a>Propriedade QueryDef.MaxRecords (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna o número máximo de registros a serem retornados de uma consulta em relação à fonte de dados ODBC.

## <a name="syntax"></a>Sintaxe

*expressão* . MaxRecords

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

O valor padrão é 0, indicando nenhum limite no número de registros retornados.

Assim que o número de linhas especificado por **MaxRecords** for retornado para o aplicativo em um **[Recordset](recordset-object-dao.md)**, o processador de consultas interromperá o retorno de registros adicionais, mesmo que mais registros estejam qualificados para inclusão no **Recordset**. Essa propriedade é útil em situações nas quais os recursos limitados do cliente proíbem o gerenciamento de uma grande quantidade de registros.

> [!NOTE]
> [!OBSERVAçãO] A propriedade **MaxRecords** pode ser usada somente em uma fonte de dados ODBC.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **MaxRecords** para definir um limite sobre quantos registros são retornados por uma consulta em uma fonte de dados do ODBC.

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

