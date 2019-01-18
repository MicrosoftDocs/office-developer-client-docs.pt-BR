---
title: Objeto Connection (ADO)
TOCTitle: Connection object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ed736a0e52ff45cd0fed63f1ba5bd7060d7a2380
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718410"
---
# <a name="connection-object-ado"></a><span data-ttu-id="04798-102">Objeto Connection (ADO)</span><span class="sxs-lookup"><span data-stu-id="04798-102">Connection object (ADO)</span></span>

<span data-ttu-id="04798-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="04798-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04798-104">Representa uma conexão aberta com uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="04798-104">Represents an open connection to a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="04798-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="04798-105">Remarks</span></span>

<span data-ttu-id="04798-p101">Um objeto **Connection** representa uma única sessão com uma fonte de dados. No caso de um sistema de banco de dados cliente/servidor, pode ser equivalente à conexão de rede real com o servidor. Dependendo da funcionalidade suportada pelo provedor, algumas coleções, métodos ou propriedades de um objeto **Connection** podem não estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="04798-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it may be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object may not be available.</span></span>

<span data-ttu-id="04798-109">Com as coleções, os métodos e as propriedades de um objeto **Connection**, você pode fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="04798-109">With the collections, methods, and properties of a **Connection** object, you can do the following:</span></span>

  - <span data-ttu-id="04798-p102">Configurar a conexão antes de abri-la com as propriedades [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md) e [Mode](mode-property-ado.md). **ConnectionString** é a propriedade padrão de um objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="04798-p102">Configure the connection before opening it with the [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md), and [Mode](mode-property-ado.md) properties. **ConnectionString** is the default property of the **Connection** object.</span></span>

  - <span data-ttu-id="04798-112">Definir a propriedade [CursorLocation](cursorlocation-property-ado.md) para o cliente chamar o [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), que suporta as atualizações em lotes.</span><span class="sxs-lookup"><span data-stu-id="04798-112">Set the [CursorLocation](cursorlocation-property-ado.md) property to client to invoke the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), which supports batch updates.</span></span>

  - <span data-ttu-id="04798-113">Definir o banco de dados padrão da conexão com a propriedade [DefaultDatabase](defaultdatabase-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04798-113">Set the default database for the connection with the [DefaultDatabase](defaultdatabase-property-ado.md) property.</span></span>

  - <span data-ttu-id="04798-114">Definir o nível de isolamento das transações abertas na conexão com a propriedade [IsolationLevel](isolationlevel-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04798-114">Set the level of isolation for the transactions opened on the connection with the [IsolationLevel](isolationlevel-property-ado.md) property.</span></span>

  - <span data-ttu-id="04798-115">Especificar um provedor do OLE DB com a propriedade [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04798-115">Specify an OLE DB provider with the [Provider](provider-property-ado.md) property.</span></span>

  - <span data-ttu-id="04798-116">Estabelecer, e mais tarde quebrar, a conexão física da fonte de dados com os métodos [Open](open-method-ado-connection.md) e [Close](close-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04798-116">Establish, and later break, the physical connection to the data source with the [Open](open-method-ado-connection.md) and [Close](close-method-ado.md) methods.</span></span>

  - <span data-ttu-id="04798-117">Executar um comando na conexão com o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) e configurar a execução com a propriedade [CommandTimeout](commandtimeout-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04798-117">Execute a command on the connection with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method and configure the execution with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="04798-p103">[!OBSERVAçãO] Para executar uma consulta sem usar o objeto Command, passe uma sequência de consulta para o método **Execute** de um objeto **Connection**. No entanto, um objeto [Command](command-object-ado.md) será necessário quando você desejar insistir no texto de comando e reexecutá-lo ou usar os parâmetros da consulta.</span><span class="sxs-lookup"><span data-stu-id="04798-p103">To execute a query without using a Command object, pass a query string to the **Execute** method of a **Connection** object. However, a [Command](command-object-ado.md) object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

  - <span data-ttu-id="04798-120">Gerenciar as transações na conexão aberta, incluindo as transações aninhadas se o provedor oferecer suporte para essas transações, com o métodos [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) e [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) e a propriedade [Attributes](attributes-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04798-120">Manage transactions on the open connection, including nested transactions if the provider supports them, with the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), and [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) methods and the [Attributes](attributes-property-ado.md) property.</span></span>

  - <span data-ttu-id="04798-121">Examinar os erros retornados da fonte de dados com a coleção [Errors](errors-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04798-121">Examine errors returned from the data source with the [Errors](errors-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="04798-122">Ler a versão da implementação ADO usada com a propriedade [Version](version-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04798-122">Read the version from the ADO implementation used with the [Version](version-property-ado.md) property.</span></span>

  - <span data-ttu-id="04798-123">Obter informações sobre o esquema do banco de dados com o método [OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04798-123">Obtain schema information about your database with the [OpenSchema](openschema-method-ado.md) method.</span></span>

<span data-ttu-id="04798-124">Crie os objetos **Connection** independentemente de qualquer outro objeto definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="04798-124">You can create **Connection** objects independently of any other previously defined object.</span></span>

<span data-ttu-id="04798-125">Execute os comandos ou procedimentos armazenados como se fossem métodos nativos no objeto **Connection**, como exemplificado a seguir.</span><span class="sxs-lookup"><span data-stu-id="04798-125">You can execute commands or stored procedures as if they were native methods on the **Connection** object, as illustrated below.</span></span>

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="04798-126">Executar um comando como um método nativo de um objeto Connection</span><span class="sxs-lookup"><span data-stu-id="04798-126">Execute a command as a native method of a Connection object</span></span>

<span data-ttu-id="04798-p104">Para executar um comando, forneça o nome dele usando o objeto **Command** da propriedade [Name](name-property-ado.md). Defina a propriedade **ActiveConnection** do objeto **Command** para a conexão. Em seguida, emita uma instrução na qual o nome do comando será usado como se fosse um método do objeto **Connection**, seguido por quaisquer parâmetros e depois por um objeto **Recordset** se quaisquer linhas forem retornadas. Defina as propriedades **Recordset** para personalizar o **Recordset** resultante. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="04798-p104">To execute a command, give the command a name using the **Command** object [Name](name-property-ado.md) property. Set the **Command** object's **ActiveConnection** property to the connection. Then issue a statement where the command name is used as if it were a method on the **Connection** object, followed by any parameters, then followed by a **Recordset** object if any rows are returned. Set the **Recordset** properties to customize the resulting **Recordset**. For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    Dim cmd As New ADODB.Command
    Dim rst As New ADODB.Recordset
    ...
    cnn.Open "..."
    cmd.Name = "yourCommandName"
    cmd.ActiveConnection = cnn
    ...
    'Your command name, any parameters, and an optional Recordset.
    cnn.yourCommandName "parameter", rst
```

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="04798-132">Executar um procedimento armazenado com um método nativo do objeto Connection</span><span class="sxs-lookup"><span data-stu-id="04798-132">Execute a stored procedure as a native method of a Connection object</span></span>

<span data-ttu-id="04798-p105">Para executar um procedimento armazenado, emita uma instrução na qual o nome do procedimento armazenado seja usado como se fosse um método do objeto **Connection**, seguido por quaisquer parâmetros. O ADO se tornará a "melhor solução" dos tipos de parâmetros. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="04798-p105">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the **Connection** object, followed by any parameters. ADO will make a "best guess" of parameter types. For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
