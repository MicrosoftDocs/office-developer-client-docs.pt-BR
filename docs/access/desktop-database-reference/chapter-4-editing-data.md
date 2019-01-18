---
title: 'Capítulo 4: Edição de dados'
TOCTitle: 'Chapter 4: Editing data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b954cf8b730a74fb7e630fbafb96c046491c6f46
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701141"
---
# <a name="chapter-4-editing-data"></a><span data-ttu-id="32b9b-102">Capítulo 4: Edição de dados</span><span class="sxs-lookup"><span data-stu-id="32b9b-102">Chapter 4: Editing data</span></span>

<span data-ttu-id="32b9b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="32b9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32b9b-p101">Os dois capítulos anteriores explicaram como usar o ADO para estabelecer conexão com uma fonte de dados, executar um comando, obter os resultados em um objeto **Recordset** e navegar no **Recordset**. Este capítulo concentra-se na próxima operação fundamental do ADO: edição de dados.</span><span class="sxs-lookup"><span data-stu-id="32b9b-p101">The preceding two chapters explained how use ADO to connect to a data source, execute a command, get the results in a **Recordset** object, and navigate within the **Recordset**. This chapter focuses on the next fundamental ADO operation: editing data.</span></span>

<span data-ttu-id="32b9b-p102">Ele continua a usar o **Recordset** de exemplo apresentado no Capítulo 3 , com uma alteração importante. O código a seguir é usado para abrir o **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="32b9b-p102">This chapter continues to use the sample **Recordset** introduced in Chapter 3 — with one important change. The following code is used to open the **Recordset**:</span></span>

```vb 
 
 . . . 
'BeginEditIntro 
 Dim strSQL As String 
 Dim objRs1 As ADODB.Recordset 
 
 strSQL = "SELECT * FROM Shippers" 
 
 Set objRs1 = New ADODB.Recordset 
 
 objRs1.Open strSQL, GetNewConnection, adOpenStatic, _ 
 adLockBatchOptimistic, adCmdText 
 
 ' Disconnect the Recordset from the Connection object. 
 Set objRs1.ActiveConnection = Nothing 
'EndEditIntro 
 
 
 . . . 
```

<span data-ttu-id="32b9b-p103">A alteração importante no código envolve a definição da propriedade **CursorLocation** do objeto **Connection** como **adUseClient** na função GetNewConnection (mostrada abaixo), que indica o uso de um cursor de cliente. Para obter mais informações sobre as diferenças entre cursores de cliente e de servidor, consulte o [Capítulo 8: Noções básicas sobre cursores e proteções](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="32b9b-p103">The important change to the code involves setting the **Connection** object's **CursorLocation** property equal to **adUseClient** in the GetNewConnection function (shown below), which indicates the use of a client cursor. For more information about the differences between client-side and server-side cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

<span data-ttu-id="32b9b-p104">A definição **adUseClient** da propriedade **CursorLocation** move o local do cursor da fonte de dados (neste caso, o SQL Server) para o local do código do cliente (a estação de trabalho desktop). Essa definição força o ADO a chamar o Client Cursor Engine para OLE DB no cliente para criar e gerenciar o cursor.</span><span class="sxs-lookup"><span data-stu-id="32b9b-p104">The **CursorLocation** property's **adUseClient** setting moves the location of the cursor from the data source (the SQL Server, in this case) to the location of the client code (the desktop workstation). This setting forces ADO to invoke the Client Cursor Engine for OLE DB on the client in order to create and manage the cursor.</span></span>

<span data-ttu-id="32b9b-p105">Você também pode ter notado que o parâmetro **LockType** do método **Open** foi alterado para **adLockBatchOptimistic**. Essa ação abre o cursor no modo em lotes. (O provedor armazena em cache várias alterações e as grava na fonte de dados subjacente somente quando o método **UpdateBatch** é chamado.) As alterações feitas no **Recordset** só serão atualizadas no banco de dados quando o método **UpdateBatch** for chamado.</span><span class="sxs-lookup"><span data-stu-id="32b9b-p105">You might also have noticed that the **LockType** parameter of the **Open** method changed to **adLockBatchOptimistic**. This opens the cursor in batch mode. (The provider caches multiple changes and writes them to the underlying data source only when you call the **UpdateBatch** method.) Changes made to the **Recordset** will not be updated in the database until the **UpdateBatch** method is called.</span></span>

<span data-ttu-id="32b9b-p106">Por fim, o código neste capítulo usa uma versão modificada da função GetNewConnection, apresentada no Capítulo 2. Agora, essa versão da função retorna um cursor do cliente. A função tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="32b9b-p106">Finally, the code in this chapter uses a modified version of the GetNewConnection function, introduced in Chapter 2. This version of the function now returns a client-side cursor. The function looks like this:</span></span>

```vb 
 
'BeginNewConnection 
Public Function GetNewConnection() As ADODB.Connection 
 Dim objConn1 As ADODB.Connection 
 Set objConn1 = New ADODB.Connection 
 
 strConnStr = "Provider=SQLOLEDB;Initial Catalog=Northwind;" & _ 
 "Data Source=MySrvr;Integrated Security=SSPI;" 
 
 objConn1.ConnectionString = strConnStr 
 objConn1.CursorLocation = adUseClient 
 objConn1.Open 
 
 Set GetNewConnection = objConn1 
End Function 
'EndNewConnection 
```

<span data-ttu-id="32b9b-118">Este capítulo aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="32b9b-118">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="32b9b-119">Edição de registros existentes</span><span class="sxs-lookup"><span data-stu-id="32b9b-119">Editing existing records</span></span>](editing-existing-records.md)
- [<span data-ttu-id="32b9b-120">Determinação do que é compatível</span><span class="sxs-lookup"><span data-stu-id="32b9b-120">Determining what is supported</span></span>](determining-what-is-supported.md)
- [<span data-ttu-id="32b9b-121">Exclusão de registros com o método Delete</span><span class="sxs-lookup"><span data-stu-id="32b9b-121">Deleting records using the Delete method</span></span>](deleting-records-using-the-delete-method.md)
- [<span data-ttu-id="32b9b-122">Alternativas: usando instruções SQL</span><span class="sxs-lookup"><span data-stu-id="32b9b-122">Alternatives: using SQL statements</span></span>](alternatives-using-sql-statements.md)
- [<span data-ttu-id="32b9b-123">Adicionando registros (ADO)</span><span class="sxs-lookup"><span data-stu-id="32b9b-123">Adding records (ADO)</span></span>](adding-records.md)
