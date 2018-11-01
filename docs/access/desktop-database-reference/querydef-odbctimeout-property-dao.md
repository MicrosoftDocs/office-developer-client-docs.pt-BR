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
ms.openlocfilehash: c335140e6b5bfa46d25d20438d8af2a9e1393644
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873667"
---
# <a name="querydefodbctimeout-property-dao"></a><span data-ttu-id="16f71-102">Propriedade QueryDef.ODBCTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="16f71-102">QueryDef.ODBCTimeout Property (DAO)</span></span>


<span data-ttu-id="16f71-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="16f71-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16f71-104">Indica se o número de segundos a ser aguardado antes da ocorrência de um erro de tempo limite durante a execução de **[QueryDef](querydef-object-dao.md)** em um banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="16f71-104">Indicates the number of seconds to wait before a timeout error occurs when a **[QueryDef](querydef-object-dao.md)** is executed on an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f71-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16f71-105">Syntax</span></span>

<span data-ttu-id="16f71-106">*expressão* . ODBCTimeout</span><span class="sxs-lookup"><span data-stu-id="16f71-106">*expression* .ODBCTimeout</span></span>

<span data-ttu-id="16f71-107">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="16f71-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f71-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="16f71-108">Remarks</span></span>

<span data-ttu-id="16f71-p101">Quando a propriedade **ODBCTimeout** for definida como -1, os padrões de tempo limite para a definição atual da propriedade **[QueryTimeout](database-querytimeout-property-dao.md)** do objeto **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)** que contém o **QueryDef**. Quando a propriedade **ODBCTimeout** for definida como 0, não ocorrerá um erro de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="16f71-p101">When the **ODBCTimeout** property is set to -1, the timeout defaults to the current setting of the **[QueryTimeout](database-querytimeout-property-dao.md)** property of the **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object that contains the **QueryDef**. When the **ODBCTimeout** property is set to 0, no timeout error occurs.</span></span>

<span data-ttu-id="16f71-p102">Quando você estiver usando um banco de dados ODBC, como o Microsoft SQL Server, poderão ocorrer atrasos por causa do tráfego de rede ou do uso intenso do servidor ODBC. Em vez de aguardar indefinidamente, especifique quanto tempo será necessário aguardar antes que seja retornado um erro.</span><span class="sxs-lookup"><span data-stu-id="16f71-p102">When you're using an ODBC database, such as Microsoft SQL Server, delays can occur because of network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait before returning an error.</span></span>

<span data-ttu-id="16f71-113">A definição da propriedade **ODBCTimeout** de um objeto **QueryDef** substituirá o valor especificado pela propriedade **QueryTimeout** do objeto **Connection** ou **Database** que contém o **QueryDef**, mas somente para esse objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="16f71-113">Setting the **ODBCTimeout** property of a **QueryDef** object overrides the value specified by the **QueryTimeout** property of the **Connection** or **Database** object containing the **QueryDef**, but only for that **QueryDef** object.</span></span>

## <a name="example"></a><span data-ttu-id="16f71-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="16f71-114">Example</span></span>

<span data-ttu-id="16f71-115">Este exemplo usa as propriedades **ODBCTimeout** e **QueryTimeout** para mostrar como a configuração de **QueryTimeout** em um objeto **Database** define a configuração padrão de **ODBCTimeout** em quaisquer objetos **QueryDef** criados a partir do objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="16f71-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

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

