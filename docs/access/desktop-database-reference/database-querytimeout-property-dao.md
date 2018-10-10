---
title: Propriedade Database.QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 247109d4f71fe153b639c9efa0e6944fb09448b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464199"
---
# <a name="databasequerytimeout-property-dao"></a>Propriedade Database.QueryTimeout (DAO)


**Aplica-se a**: Access 2013 | Office 2013


Define ou retorna um valor que especifica o número de segundos a serem aguardados antes de ocorrer um erro de tempo limite quando uma consulta é executada em uma fonte de dados ODBC.

## <a name="syntax"></a>Sintaxe

*expressão* . QueryTimeout

*expressão* Uma variável que representa um objeto de **banco de dados** .

## <a name="remarks"></a>Comentários

O valor padrão é 60.

Quando você está utilizando um banco de dados ODBC, como o Microsoft SQL Server, pode haver atrasos devido ao tráfego da rede ou ao uso pesado do servidor ODBC. Em vez aguardar por um tempo indefinido, você poderá especificar o tempo de espera.

Quando você usa **QueryTimeout** com um objeto **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, ele especifica um valor global para todas as consultas associadas ao banco de dados. Você pode substituir esse valor por uma consulta específica, definindo a propriedade **ODBCTimeout** de um determinado objeto **[QueryDef](querydef-object-dao.md)**.

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

