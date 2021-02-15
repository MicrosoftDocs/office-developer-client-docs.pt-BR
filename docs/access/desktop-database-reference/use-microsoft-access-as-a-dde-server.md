---
title: Usar o Microsoft Access como um servidor DDE
TOCTitle: Use Microsoft Access as a DDE Server
description: O Microsoft Access dá suporte à DDE (troca dinâmica de dados) como um aplicativo de destino (cliente) ou um aplicativo de origem (servidor).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0750bdce0e1cda383c48f9c16e62e00997fdfb0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313388"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="60ecb-103">Usar o Microsoft Access como um servidor DDE</span><span class="sxs-lookup"><span data-stu-id="60ecb-103">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="60ecb-104">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60ecb-104">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="60ecb-p101">O Microsoft Access dá suporte à DDE (troca dinâmica de dados) como um aplicativo de destino (cliente) ou um aplicativo de origem (servidor). Por exemplo, um aplicativo como Microsoft Word, funcionando como um cliente, pode solicitar dados através da DDE de um banco de dados do Microsoft Access que esteja funcionando como servidor.</span><span class="sxs-lookup"><span data-stu-id="60ecb-p101">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application. For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="60ecb-107">[!DICA] Caso você precise manipular objetos do Microsoft Access a partir de outro aplicativo, convém considerar o uso da Automação.</span><span class="sxs-lookup"><span data-stu-id="60ecb-107">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="60ecb-108">Uma conversação DDE entre um cliente e servidor é estabelecida em um tópico específico.</span><span class="sxs-lookup"><span data-stu-id="60ecb-108">A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="60ecb-109">Um tópico pode ser um arquivo de dados em um formato com suporte do aplicativo servidor ou o tópico System, que fornece informações sobre o próprio aplicativo servidor.</span><span class="sxs-lookup"><span data-stu-id="60ecb-109">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="60ecb-110">Depois que uma conversa tiver começado em um tópico específico, somente um item de dados associado a esse tópico poderá ser transferido.</span><span class="sxs-lookup"><span data-stu-id="60ecb-110">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="60ecb-p103">Por exemplo, suponha que você esteja executando o Microsoft Word e queira inserir dados de um banco de dados específico do Microsoft Access em um documento. Comece uma conversação DDE com o Microsoft Access abrindo um canal DDE com a função **DDEInitiate** e especificando o nome do arquivo de banco de dados como o tópico. Em seguida, será transferir os dados daquele banco de dados para o Microsoft Word por meio desse canal.</span><span class="sxs-lookup"><span data-stu-id="60ecb-p103">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document. You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic. You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="60ecb-114">Como um servidor DDE, o Microsoft Access dá suporte a estes tópicos:</span><span class="sxs-lookup"><span data-stu-id="60ecb-114">As a DDE server, Microsoft Access supports the following topics:</span></span>

- <span data-ttu-id="60ecb-115">O tópico System</span><span class="sxs-lookup"><span data-stu-id="60ecb-115">The System topic</span></span>

- <span data-ttu-id="60ecb-116">O nome de um banco de dados (tópico *database*)</span><span class="sxs-lookup"><span data-stu-id="60ecb-116">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="60ecb-117">O nome de uma tabela (tópico *tablename*)</span><span class="sxs-lookup"><span data-stu-id="60ecb-117">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="60ecb-118">O nome de uma consulta (tópico *queryname*)</span><span class="sxs-lookup"><span data-stu-id="60ecb-118">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="60ecb-119">Uma cadeia SQL do Microsoft Access (tópico *sqlstring*)</span><span class="sxs-lookup"><span data-stu-id="60ecb-119">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="60ecb-120">Depois de estabelecer uma conversação DDE, você pode usar a instrução **DDEExecute** para enviar um comando do cliente para o aplicativo servidor.</span><span class="sxs-lookup"><span data-stu-id="60ecb-120">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="60ecb-121">Quando usado como um servidor DDE, o Microsoft Access reconhece qualquer um destes como comandos válidos:</span><span class="sxs-lookup"><span data-stu-id="60ecb-121">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="60ecb-122">O nome de uma macro no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="60ecb-122">The name of a macro in the current database.</span></span>

- <span data-ttu-id="60ecb-123">Qualquer ação executável no Visual Basic através de um dos métodos do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="60ecb-123">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="60ecb-p105">As ações AbrirBancoDeDados e FecharBancoDeDados, usadas somente para operações DDE. (Um exemplo de como usar essas ações encontra-se adiante neste tópico).</span><span class="sxs-lookup"><span data-stu-id="60ecb-p105">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="60ecb-p106">[!OBSERVAçãO] Quando você especifica uma ação de macro como uma instrução **DDEExecute**, a ação e quaisquer argumentos seguem a sintaxe do objeto **DoCmd** e precisam vir entre colchetes ([ ]). No entanto, aplicativos que dão suporte à DDE não reconhecem constantes intrínsecas em operações DDE. Além disso, argumentos de cadeias de caracteres precisam vir entre aspas (" ") se a cadeia contiver uma vírgula. Senão, as aspas são desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="60ecb-p106">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="60ecb-130">O aplicativo cliente pode usar a função **DDERequest** para solicitar dados de texto do aplicativo servidor através de um canal DDE aberto.</span><span class="sxs-lookup"><span data-stu-id="60ecb-130">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="60ecb-131">Outra alternativa é o cliente usar a instrução **DDEPoke** para enviar dados ao aplicativo servidor.</span><span class="sxs-lookup"><span data-stu-id="60ecb-131">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="60ecb-132">Após a conclusão da transferência de dados, o cliente pode usar a instrução **DDETerminate** para fechar o canal DDE ou a instrução **DDETerminateAll** para fechar todos os canais abertos.</span><span class="sxs-lookup"><span data-stu-id="60ecb-132">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="60ecb-133">[!OBSERVAçãO] Quando o aplicativo cliente termina de receber dados através de um canal DDE, deve fechar aquele canal para poupar recursos de memória.</span><span class="sxs-lookup"><span data-stu-id="60ecb-133">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>

<span data-ttu-id="60ecb-p108">O exemplo a seguir demonstra como criar um procedimento do Microsoft Word com Visual Basic que usa o Microsoft Access como um servidor DDE. (Para este exemplo funcionar, o Microsoft Access deve estar sendo executado).</span><span class="sxs-lookup"><span data-stu-id="60ecb-p108">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server. (For this example to work, Microsoft Access must be running.)</span></span>

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<br/>

<span data-ttu-id="60ecb-136">As seções a seguir fornecem informações sobre os tópicos DDE válidos com suporte do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="60ecb-136">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="60ecb-137">O tópico System</span><span class="sxs-lookup"><span data-stu-id="60ecb-137">The System topic</span></span>

<span data-ttu-id="60ecb-138">O tópico System é um tópico padrão para todos os aplicativos baseados no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="60ecb-138">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="60ecb-139">Ele fornece informações sobre os outros tópicos com suporte do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60ecb-139">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="60ecb-140">Para acessar essas informações, seu código deve primeiro chamar  a função **DDEInitiate** com o argumento de tópico e, em seguida, executar a instrução **DDERequest** com um dos seguintes fornecidos para o argumento *do item.*</span><span class="sxs-lookup"><span data-stu-id="60ecb-140">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60ecb-141">Item</span><span class="sxs-lookup"><span data-stu-id="60ecb-141">Item</span></span></p></th>
<th><p><span data-ttu-id="60ecb-142">Retorna</span><span class="sxs-lookup"><span data-stu-id="60ecb-142">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-143">SysItems</span><span class="sxs-lookup"><span data-stu-id="60ecb-143">SysItems</span></span></p></td>
<td><p><span data-ttu-id="60ecb-144">Uma lista de itens com suporte do tópico Sistema no Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="60ecb-144">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-145">Formats</span><span class="sxs-lookup"><span data-stu-id="60ecb-145">Formats</span></span></p></td>
<td><p><span data-ttu-id="60ecb-146">Uma lista dos formatos que o Microsoft Access consegue copiar para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="60ecb-146">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-147">Status</span><span class="sxs-lookup"><span data-stu-id="60ecb-147">Status</span></span></p></td>
<td><p><span data-ttu-id="60ecb-148">&quot;Ocupado &quot; ou &quot; &quot; Pronto.</span><span class="sxs-lookup"><span data-stu-id="60ecb-148">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-149">Topics</span><span class="sxs-lookup"><span data-stu-id="60ecb-149">Topics</span></span></p></td>
<td><p><span data-ttu-id="60ecb-150">Uma lista de todos os bancos de dados abertos.</span><span class="sxs-lookup"><span data-stu-id="60ecb-150">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="60ecb-151">O exemplo a seguir demonstra o uso das funções **DDEInitiate** e **DDERequest** com o tópico System:</span><span class="sxs-lookup"><span data-stu-id="60ecb-151">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a><span data-ttu-id="60ecb-152">O tópico do banco de dados</span><span class="sxs-lookup"><span data-stu-id="60ecb-152">The database topic</span></span>

<span data-ttu-id="60ecb-153">O tópico *database* é o nome do arquivo de um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="60ecb-153">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="60ecb-154">Você pode digitar apenas o nome base (Northwind) ou seu caminho e extensão .mdb (C: Exemplos do \\ Access \\ \\ Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="60ecb-154">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="60ecb-155">Após iniciar uma conversação DDE com o banco de dados, você pode solicitar uma lista dos objetos naquele banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60ecb-155">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

> [!NOTE]
> <span data-ttu-id="60ecb-156">Não é possível usar a DDE para consultar o arquivo de informações do grupo de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="60ecb-156">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>

<span data-ttu-id="60ecb-157">O tópico *database* oferece suporte aos seguintes itens.</span><span class="sxs-lookup"><span data-stu-id="60ecb-157">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60ecb-158">Item</span><span class="sxs-lookup"><span data-stu-id="60ecb-158">Item</span></span></p></th>
<th><p><span data-ttu-id="60ecb-159">Retorna</span><span class="sxs-lookup"><span data-stu-id="60ecb-159">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-160">TableList</span><span class="sxs-lookup"><span data-stu-id="60ecb-160">TableList</span></span></p></td>
<td><p><span data-ttu-id="60ecb-161">Uma lista de tabelas</span><span class="sxs-lookup"><span data-stu-id="60ecb-161">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-162">QueryList</span><span class="sxs-lookup"><span data-stu-id="60ecb-162">QueryList</span></span></p></td>
<td><p><span data-ttu-id="60ecb-163">Uma lista de consultas</span><span class="sxs-lookup"><span data-stu-id="60ecb-163">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-164">FormList</span><span class="sxs-lookup"><span data-stu-id="60ecb-164">FormList</span></span></p></td>
<td><p><span data-ttu-id="60ecb-165">Uma lista de formulários</span><span class="sxs-lookup"><span data-stu-id="60ecb-165">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-166">ReportList</span><span class="sxs-lookup"><span data-stu-id="60ecb-166">ReportList</span></span></p></td>
<td><p><span data-ttu-id="60ecb-167">Uma lista de relatórios</span><span class="sxs-lookup"><span data-stu-id="60ecb-167">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-168">MacroList</span><span class="sxs-lookup"><span data-stu-id="60ecb-168">MacroList</span></span></p></td>
<td><p><span data-ttu-id="60ecb-169">Uma lista de macros</span><span class="sxs-lookup"><span data-stu-id="60ecb-169">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-170">ModuleList</span><span class="sxs-lookup"><span data-stu-id="60ecb-170">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="60ecb-171">Uma lista de módulos</span><span class="sxs-lookup"><span data-stu-id="60ecb-171">A list of modules</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-172">ViewList</span><span class="sxs-lookup"><span data-stu-id="60ecb-172">ViewList</span></span></p></td>
<td><p><span data-ttu-id="60ecb-173">Uma lista de modos.</span><span class="sxs-lookup"><span data-stu-id="60ecb-173">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-174">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="60ecb-174">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="60ecb-175">Uma lista de procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="60ecb-175">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-176">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="60ecb-176">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="60ecb-177">Uma lista de diagramas de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="60ecb-177">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="60ecb-178">O exemplo a seguir mostra como abrir o formulário Employees no exemplo de banco de dados Northwind a partir de um procedimento do Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="60ecb-178">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a><span data-ttu-id="60ecb-179">O tópico TABLE</span><span class="sxs-lookup"><span data-stu-id="60ecb-179">The TABLE topic</span></span>

<span data-ttu-id="60ecb-180">Esses tópicos usam a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="60ecb-180">These topics use the following syntax:</span></span>

<span data-ttu-id="60ecb-181">_databasename_ ; **TABLE** _tablename_</span><span class="sxs-lookup"><span data-stu-id="60ecb-181">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="60ecb-182">_databasename_ ; **QUERY** _queryname_</span><span class="sxs-lookup"><span data-stu-id="60ecb-182">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="60ecb-183">_databasename_ ; **SQL** [ _sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="60ecb-183">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60ecb-184">Sair</span><span class="sxs-lookup"><span data-stu-id="60ecb-184">Part</span></span></p></th>
<th><p><span data-ttu-id="60ecb-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="60ecb-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-186"><em>databasename</em></span><span class="sxs-lookup"><span data-stu-id="60ecb-186"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="60ecb-p111">O nome do banco de dados em que está a tabela ou consulta ou a que se aplica o SQL, seguido de ponto-e-vírgula (;). O nome do banco de dados pode ser apenas o nome básico (Northwind) ou seu caminho e extensão .mdb completos (C:\Access\Exemplos\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="60ecb-p111">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;). The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-189"><em>tablename</em></span><span class="sxs-lookup"><span data-stu-id="60ecb-189"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="60ecb-190">O nome de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="60ecb-190">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-191"><em>queryname</em></span><span class="sxs-lookup"><span data-stu-id="60ecb-191"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="60ecb-192">O nome de uma consulta existente.</span><span class="sxs-lookup"><span data-stu-id="60ecb-192">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-193"><em>sqlstring</em></span><span class="sxs-lookup"><span data-stu-id="60ecb-193"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="60ecb-194">Uma instrução SQL válida com até 256 caracteres e terminando com ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="60ecb-194">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="60ecb-195">Para trocar mais de 256 caracteres, omita esse argumento e, em seu lugar, use sucessivas instruções <strong>DDEPoke</strong> para formar uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="60ecb-195">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="60ecb-196">Por exemplo, o seguinte código Visual Basic utiliza a instrução <strong>DDEPoke</strong> para formar uma instrução SQL e, em seguida, solicitar os resultados de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="60ecb-196">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="60ecb-197">A tabela a seguir lista os itens válidos para os tópicos TABELA *tablename*, CONSULTA *queryname* e SQL *sqlstring*.</span><span class="sxs-lookup"><span data-stu-id="60ecb-197">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60ecb-198">Item</span><span class="sxs-lookup"><span data-stu-id="60ecb-198">Item</span></span></p></th>
<th><p><span data-ttu-id="60ecb-199">Retorna</span><span class="sxs-lookup"><span data-stu-id="60ecb-199">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-200">Todos</span><span class="sxs-lookup"><span data-stu-id="60ecb-200">All</span></span></p></td>
<td><p><span data-ttu-id="60ecb-201">Todos os dados na tabela, incluindo nomes de campos.</span><span class="sxs-lookup"><span data-stu-id="60ecb-201">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-202">Dados</span><span class="sxs-lookup"><span data-stu-id="60ecb-202">Data</span></span></p></td>
<td><p><span data-ttu-id="60ecb-203">Todas as linhas de dados, sem nomes de campos.</span><span class="sxs-lookup"><span data-stu-id="60ecb-203">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-204">FieldNames</span><span class="sxs-lookup"><span data-stu-id="60ecb-204">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="60ecb-205">Uma lista de linha única de nomes de campos.</span><span class="sxs-lookup"><span data-stu-id="60ecb-205">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-206">FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="60ecb-206">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="60ecb-207">Uma lista de duas linhas de nomes de campos (primeira linha) e seus tipos de dados (segunda linha).</span><span class="sxs-lookup"><span data-stu-id="60ecb-207">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="60ecb-208">Estes são os valores retornados:</span><span class="sxs-lookup"><span data-stu-id="60ecb-208">These are the values returned:</span></span></p>
<p><span data-ttu-id="60ecb-209">Valor</span><span class="sxs-lookup"><span data-stu-id="60ecb-209">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="60ecb-210">0</span><span class="sxs-lookup"><span data-stu-id="60ecb-210">0</span></span></li>
<li><span data-ttu-id="60ecb-211">1 </span><span class="sxs-lookup"><span data-stu-id="60ecb-211">1</span></span></li>
<li><span data-ttu-id="60ecb-212">2 </span><span class="sxs-lookup"><span data-stu-id="60ecb-212">2</span></span></li>
<li><span data-ttu-id="60ecb-213">3 </span><span class="sxs-lookup"><span data-stu-id="60ecb-213">3</span></span></li>
<li><span data-ttu-id="60ecb-214">4 </span><span class="sxs-lookup"><span data-stu-id="60ecb-214">4</span></span></li>
<li><span data-ttu-id="60ecb-215">5 </span><span class="sxs-lookup"><span data-stu-id="60ecb-215">5</span></span></li>
<li><span data-ttu-id="60ecb-216">6 </span><span class="sxs-lookup"><span data-stu-id="60ecb-216">6</span></span></li>
<li><span data-ttu-id="60ecb-217">7 </span><span class="sxs-lookup"><span data-stu-id="60ecb-217">7</span></span></li>
<li><span data-ttu-id="60ecb-218">8 </span><span class="sxs-lookup"><span data-stu-id="60ecb-218">8</span></span></li>
<li><span data-ttu-id="60ecb-219">9 </span><span class="sxs-lookup"><span data-stu-id="60ecb-219">9</span></span></li>
<li><span data-ttu-id="60ecb-220">10 </span><span class="sxs-lookup"><span data-stu-id="60ecb-220">10</span></span></li>
<li><span data-ttu-id="60ecb-221">11</span><span class="sxs-lookup"><span data-stu-id="60ecb-221">11</span></span></li>
<li><span data-ttu-id="60ecb-222">12 </span><span class="sxs-lookup"><span data-stu-id="60ecb-222">12</span></span></li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-223">NextRow</span><span class="sxs-lookup"><span data-stu-id="60ecb-223">NextRow</span></span></p></td>
<td><p><span data-ttu-id="60ecb-p113">Os dados na próxima linha da tabela ou consulta. Quando você abre um canal, NextRow retorna os dados da primeira linha. Se a linha atual for o último registro e você executar NextRow, a solicitação falhará.</span><span class="sxs-lookup"><span data-stu-id="60ecb-p113">The data in the next row in the table or query. When you open a channel, NextRow returns the data in the first row. If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-227">PrevRow</span><span class="sxs-lookup"><span data-stu-id="60ecb-227">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="60ecb-p114">Os dados na linha anterior da tabela ou consulta. Se PrevRow for a primeira solicitação em um novo canal, os dados na última linha da tabela ou consulta serão retornados. Se o primeiro registro for a linha atual, a solicitação a PrevRow falhará.</span><span class="sxs-lookup"><span data-stu-id="60ecb-p114">The data in the previous row in the table or query. If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned. If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-231">FirstRow</span><span class="sxs-lookup"><span data-stu-id="60ecb-231">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="60ecb-232">Os dados na primeira linha da tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="60ecb-232">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-233">LastRow</span><span class="sxs-lookup"><span data-stu-id="60ecb-233">LastRow</span></span></p></td>
<td><p><span data-ttu-id="60ecb-234">Os dados na última linha da tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="60ecb-234">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-235">FieldCount</span><span class="sxs-lookup"><span data-stu-id="60ecb-235">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="60ecb-236">O número de campos na tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="60ecb-236">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60ecb-237">SQLText</span><span class="sxs-lookup"><span data-stu-id="60ecb-237">SQLText</span></span></p></td>
<td><p><span data-ttu-id="60ecb-238">Uma instrução SQL representando a tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="60ecb-238">An SQL statement representing the table or query.</span></span> <span data-ttu-id="60ecb-239">Para tabelas, este item retorna uma instrução SQL no formato &quot; SELECT `*` FROM <em>tabela</em>; &quot; .</span><span class="sxs-lookup"><span data-stu-id="60ecb-239">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60ecb-240">SQLText; <em>n</em></span><span class="sxs-lookup"><span data-stu-id="60ecb-240">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="60ecb-241">Uma instrução SQL, em partes de <em>n</em> caracteres, representando a tabela ou consulta, onde <em>n</em> é um inteiro de até 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="60ecb-241">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="60ecb-242">Por exemplo, suponha que uma consulta seja representada pela seguinte instrução SQL: O item SQLText;7 retorna as seguintes partes delimitadas por tabulação: O &quot; &quot; item &quot; SQLText;7 retorna as seguintes partes delimitadas por &quot; tabulação:</span><span class="sxs-lookup"><span data-stu-id="60ecb-242">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="60ecb-243">O exemplo a seguir mostra como usar DDE em um procedimento do Visual Basic para solicitar dados de uma tabela no exemplo de banco de dados Northwind e inserir os dados em um arquivo de texto:</span><span class="sxs-lookup"><span data-stu-id="60ecb-243">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
