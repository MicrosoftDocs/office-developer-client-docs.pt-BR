---
title: Propriedade QueryDef.ODBCTimeout (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ceb3cf0fa2e16af4df23c6511fd6d1421487a409
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922752"
---
# <a name="querydefodbctimeout-property-dao"></a>Propriedade QueryDef.ODBCTimeout (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Indica se o número de segundos a ser aguardado antes da ocorrência de um erro de tempo limite durante a execução de **[QueryDef](querydef-object-dao.md)** em um banco de dados ODBC.

## <a name="syntax"></a>Sintaxe

*expressão* . ODBCTimeout

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

Quando a propriedade **ODBCTimeout** for definida como -1, os padrões de tempo limite para a definição atual da propriedade **[QueryTimeout](database-querytimeout-property-dao.md)** do objeto **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)** que contém o **QueryDef**. Quando a propriedade **ODBCTimeout** for definida como 0, não ocorrerá um erro de tempo limite.

Quando você estiver usando um banco de dados ODBC, como o Microsoft SQL Server, poderão ocorrer atrasos por causa do tráfego de rede ou do uso intenso do servidor ODBC. Em vez de aguardar indefinidamente, especifique quanto tempo será necessário aguardar antes que seja retornado um erro.

A definição da propriedade **ODBCTimeout** de um objeto **QueryDef** substituirá o valor especificado pela propriedade **QueryTimeout** do objeto **Connection** ou **Database** que contém o **QueryDef**, mas somente para esse objeto **QueryDef**.

## <a name="example"></a>Exemplo

Este exemplo usa as propriedades **ODBCTimeout** e **QueryTimeout** para mostrar como a configuração de **QueryTimeout** em um objeto **Database** define a configuração padrão de **ODBCTimeout** em quaisquer objetos **QueryDef** criados a partir do objeto **Database**.

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

