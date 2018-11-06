---
title: 'Etapa 6: As alterações são enviadas ao servidor (tutorial RDS)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9f75e5215e3e3d79363ab7110f7c16bcacf3cbb
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998991"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a><span data-ttu-id="c1de4-102">Etapa 6: As alterações são enviadas ao servidor (Tutorial RDS)</span><span class="sxs-lookup"><span data-stu-id="c1de4-102">Step 6: Changes are sent to the server (RDS Tutorial)</span></span>

<span data-ttu-id="c1de4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1de4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1de4-104">Se o objeto **Recordset** for editado, todas as alterações (ou seja, linhas que são incluídas, alteradas ou excluídas) poderão ser enviadas de volta ao servidor.</span><span class="sxs-lookup"><span data-stu-id="c1de4-104">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="c1de4-105">[!OBSERVAçãO] O comportamento padrão do RDS pode ser chamado implicitamente com os objetos ADO e o Microsoft OLE DB Remoting Provider.</span><span class="sxs-lookup"><span data-stu-id="c1de4-105">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="c1de4-106">Consultas podem retornar **Recordsets**e editado **Recordsets** pode atualizar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="c1de4-106">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="c1de4-107">Esse tutorial não chama o RDS com objetos ADO, mas veja como seria se o fizesse:</span><span class="sxs-lookup"><span data-stu-id="c1de4-107">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

<span data-ttu-id="c1de4-108">**Parte A**</span><span class="sxs-lookup"><span data-stu-id="c1de4-108">**Part A**</span></span> 

<span data-ttu-id="c1de4-109">Supor que, nesse caso, que você usou apenas o [RDS. DataControl](datacontrol-object-rds.md) e se um objeto **Recordset** é agora associado a **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="c1de4-109">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="c1de4-110">O método [SubmitChanges](submitchanges-method-rds.md) atualiza a origem de dados com todas as alterações ao objeto **Recordset** se as propriedades [Server](server-property-rds.md) e [Connect](connect-property-rds.md) ainda estiverem definidas.</span><span class="sxs-lookup"><span data-stu-id="c1de4-110">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

<span data-ttu-id="c1de4-111">**Parte B**</span><span class="sxs-lookup"><span data-stu-id="c1de4-111">**Part B**</span></span> 

<span data-ttu-id="c1de4-112">Como alternativa, você poderia atualizar o servidor com o objeto [rdsserver. DataFactory](datafactory-object-rdsserver.md) , especificando uma conexão e um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c1de4-112">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```

<span data-ttu-id="c1de4-113">**Esse é o fim do tutorial.**</span><span class="sxs-lookup"><span data-stu-id="c1de4-113">**This is the end of the tutorial.**</span></span>

