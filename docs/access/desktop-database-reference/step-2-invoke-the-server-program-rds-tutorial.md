---
title: 'Etapa 2: Chamar o programa do servidor (tutorial RDS)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d3264c58434bf7af6ae4e75c249a7009f39b7d4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947228"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a><span data-ttu-id="f5af3-102">Etapa 2: Chamar o programa do servidor (Tutorial RDS)</span><span class="sxs-lookup"><span data-stu-id="f5af3-102">Step 2: Invoke the server program (RDS Tutorial)</span></span>

<span data-ttu-id="f5af3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5af3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5af3-p101">Ao chamar um método no *proxy* do cliente, o programa real no servidor executa o método. Nessa etapa, você executará uma consulta no servidor.</span><span class="sxs-lookup"><span data-stu-id="f5af3-p101">When you invoke a method on the client *proxy*, the actual program on the server executes the method. In this step, you'll execute a query on the server.</span></span>

<span data-ttu-id="f5af3-106">**Parte A** Se você não estava usando [Rdsserver](datafactory-object-rdsserver.md) neste tutorial, a maneira mais conveniente executar esta etapa seria usar o [RDS. DataControl](datacontrol-object-rds.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="f5af3-106">**Part A**If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="f5af3-107">O **RDS.DataControl** combina a etapa anterior da criação de um proxy, com essa etapa, emitindo a consulta.</span><span class="sxs-lookup"><span data-stu-id="f5af3-107">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

<span data-ttu-id="f5af3-p103">Defina a propriedade **Server** do objeto [RDS.DataControl](server-property-rds.md) para identificar onde o programa do servidor deve ser instanciado; a propriedade [Connect](connect-property-rds.md) para especificar a cadeia de conexão para acessar a origem de dados; e a propriedade [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) para especificar o texto do comando de consulta. Em seguida emita o método [Refresh](refresh-method-rds.md) para fazer com que o programa do servidor se conecte à origem de dados, recuperar as linhas especificadas pela consulta e retornar um objeto **Recordset** ao cliente.</span><span class="sxs-lookup"><span data-stu-id="f5af3-p103">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated; the [Connect](connect-property-rds.md) property to specify the connect string to access the data source; and the [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) property to specify the query command text. Then issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="f5af3-110">Este tutorial não usa o **RDS.DataControl**, mas veja como seria se o fizesse:</span><span class="sxs-lookup"><span data-stu-id="f5af3-110">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<span data-ttu-id="f5af3-111">Ele também não invoca RDS com objetos ADO, mas veja como seria se o fizesse:</span><span class="sxs-lookup"><span data-stu-id="f5af3-111">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

<span data-ttu-id="f5af3-112">**Parte B** O método geral para realizar esta etapa é invocar o método [Query](query-method-rds.md) do objeto **Rdsserver** .</span><span class="sxs-lookup"><span data-stu-id="f5af3-112">**Part B**The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="f5af3-113">Esse método assume uma cadeia de conexão, que é usada para se conectar a uma origem de dados e um texto de comando, que é usada para especificar as linhas a serem retornadas a partir da origem de dados.</span><span class="sxs-lookup"><span data-stu-id="f5af3-113">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="f5af3-114">Este tutorial usa o método **Query** do objeto **DataFactory**:</span><span class="sxs-lookup"><span data-stu-id="f5af3-114">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

