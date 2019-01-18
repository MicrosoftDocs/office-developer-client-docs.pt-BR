---
title: Propriedade Database.QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f47d6c51079bf36cb7e1ca596a3476f1a7219c5d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713510"
---
# <a name="databasequerytimeout-property-dao"></a><span data-ttu-id="edacf-102">Propriedade Database.QueryTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="edacf-102">Database.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="edacf-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="edacf-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="edacf-104">Define ou retorna um valor que especifica o número de segundos a serem aguardados antes de ocorrer um erro de tempo limite quando uma consulta é executada em uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="edacf-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="edacf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edacf-105">Syntax</span></span>

<span data-ttu-id="edacf-106">*expressão* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="edacf-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="edacf-107">*expressão* Uma variável que representa um objeto de **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="edacf-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="edacf-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="edacf-108">Remarks</span></span>

<span data-ttu-id="edacf-109">O valor padrão é 60.</span><span class="sxs-lookup"><span data-stu-id="edacf-109">The default value is 60.</span></span>

<span data-ttu-id="edacf-p101">Quando você está utilizando um banco de dados ODBC, como o Microsoft SQL Server, pode haver atrasos devido ao tráfego da rede ou ao uso pesado do servidor ODBC. Em vez aguardar por um tempo indefinido, você poderá especificar o tempo de espera.</span><span class="sxs-lookup"><span data-stu-id="edacf-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="edacf-p102">Quando você usa **QueryTimeout** com um objeto **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, ele especifica um valor global para todas as consultas associadas ao banco de dados. Você pode substituir esse valor por uma consulta específica, definindo a propriedade **ODBCTimeout** de um determinado objeto **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="edacf-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="example"></a><span data-ttu-id="edacf-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="edacf-114">Example</span></span>

<span data-ttu-id="edacf-115">Este exemplo usa as propriedades **ODBCTimeout** e **QueryTimeout** para mostrar como a configuração de **QueryTimeout** em um objeto **Database** define a configuração padrão de **ODBCTimeout** em quaisquer objetos **QueryDef** criados a partir do objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="edacf-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

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

