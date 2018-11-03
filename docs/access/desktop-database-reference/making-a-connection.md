---
title: Fazendo uma conexão
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0335c4bbc0d1240d6d4ca53ceacf47bf44fce67d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945884"
---
# <a name="making-a-connection"></a><span data-ttu-id="d186f-102">Fazendo uma conexão</span><span class="sxs-lookup"><span data-stu-id="d186f-102">Making a connection</span></span>

<span data-ttu-id="d186f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d186f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d186f-p101">Para se conectar à fonte de dados, especifique uma *sequência de caracteres de conexão* e os parâmetros para diferenciar cada provedor ou fonte de dados. Para obter mais informações, consulte [Criando uma sequência de caracteres de conexão](creating-the-connection-string.md).</span><span class="sxs-lookup"><span data-stu-id="d186f-p101">To connect to a data source, you must specify a *connection string*, the parameters of which might differ for each provider and data source. For more information, see [Creating the Connection String](creating-the-connection-string.md).</span></span>

<span data-ttu-id="d186f-p102">Geralmente, o ADO abre uma conexão usando o objeto **Connection** do método **Open**. A sintaxe do método **Open** é apresentada a seguir:</span><span class="sxs-lookup"><span data-stu-id="d186f-p102">ADO most commonly opens a connection by using the **Connection** object **Open** method. The syntax for the **Open** method is shown here:</span></span>

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

<span data-ttu-id="d186f-108">De forma alternativa, você pode chamar a técnica de atalho, **Recordset.Open**, para abrir uma conexão implícita e emitir um comando sobre aquela conexão em uma operação.</span><span class="sxs-lookup"><span data-stu-id="d186f-108">Alternatively, you can invoke a shortcut technique, **Recordset.Open**, to open an implicit connection and issue a command over that connection in one operation.</span></span> <span data-ttu-id="d186f-109">Faça isso passando uma cadeia de caracteres de conexão válida como o argumento *ActiveConnection* do método **Open** .</span><span class="sxs-lookup"><span data-stu-id="d186f-109">Do this by passing in a valid connection string as the *ActiveConnection* argument to the **Open** method.</span></span> <span data-ttu-id="d186f-110">Esta é a sintaxe de cada método do Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d186f-110">Here is the syntax for each method in Visual Basic:</span></span>

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> <span data-ttu-id="d186f-p104">[!OBSERVAçãO] Quando devo usar um objeto **Connection** versus o atalho **Recordset.Open** ? Use o objeto **Connection** se você planeja abrir mais de um **Recordset** ou quando executar vários comandos. Uma conexão ainda será criada pelo ADO de forma implícita, quando você usar o atalho **Recordset.Open**.</span><span class="sxs-lookup"><span data-stu-id="d186f-p104">When should you use a **Connection** object vs. the **Recordset.Open** shortcut? Use the **Connection** object if you plan to open more than one **Recordset**, or when executing multiple commands. A connection is still created by ADO implicitly when you use the **Recordset.Open** shortcut.</span></span>


