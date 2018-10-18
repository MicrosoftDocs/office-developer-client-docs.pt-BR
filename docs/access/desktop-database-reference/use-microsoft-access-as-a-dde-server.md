---
<span data-ttu-id="5999f-101">título: usar o Microsoft Access como um servidor DDE TOCTitle: usar o Microsoft Access como um servidor DDE <<<<<<< ms:assetid cabeça: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: ms.date 48546801: 18/09/2015 === Descrição: Microsoft Access oferece suporte a intercâmbio dinâmico de dados (DDE) como um aplicativo de destino (cliente) ou um aplicativo de origem (servidor).</span><span class="sxs-lookup"><span data-stu-id="5999f-101">title: Use Microsoft Access as a DDE server TOCTitle: Use Microsoft Access as a DDE Server <<<<<<< HEAD ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 09/18/2015 ======= description: Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application.</span></span>  
<span data-ttu-id="5999f-102">MS:AssetID: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: ms.date 48546801: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="5999f-102">ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: 48546801 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="5999f-103">mtps_version mestre: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="5999f-103">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="5999f-104">vbaac10.chm5186349 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="5999f-104">vbaac10.chm5186349 f1_categories:</span></span>
- <span data-ttu-id="5999f-105">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="5999f-105">Office.Version=v15</span></span>
---

# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="5999f-106">Usar o Microsoft Access como um servidor DDE</span><span class="sxs-lookup"><span data-stu-id="5999f-106">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="5999f-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5999f-107">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="5999f-p101">O Microsoft Access dá suporte à DDE (troca dinâmica de dados) como um aplicativo de destino (cliente) ou um aplicativo de origem (servidor). Por exemplo, um aplicativo como Microsoft Word, funcionando como um cliente, pode solicitar dados através da DDE de um banco de dados do Microsoft Access que esteja funcionando como servidor.</span><span class="sxs-lookup"><span data-stu-id="5999f-p101">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application. For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="5999f-110">[!DICA] Caso você precise manipular objetos do Microsoft Access a partir de outro aplicativo, convém considerar o uso da Automação.</span><span class="sxs-lookup"><span data-stu-id="5999f-110">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="5999f-111"><<<<<<< Conversação DDE de uma de cabeça entre um cliente e servidor é estabelecida em um tópico específico.</span><span class="sxs-lookup"><span data-stu-id="5999f-111"><<<<<<< HEAD A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="5999f-112">Um tópico pode ser um arquivo de dados em um formato com suporte do aplicativo servidor ou o tópico System, que fornece informações sobre o próprio aplicativo servidor.</span><span class="sxs-lookup"><span data-stu-id="5999f-112">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="5999f-113">Uma vez iniciada uma conversação sobre um tópico específico, somente um item de dado associado àquele tópico pode ser transferido.</span><span class="sxs-lookup"><span data-stu-id="5999f-113">Once a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>
<span data-ttu-id="5999f-114">=== Uma conversação DDE entre um cliente e servidor é estabelecida em um tópico específico.</span><span class="sxs-lookup"><span data-stu-id="5999f-114">======= A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="5999f-115">Um tópico pode ser um arquivo de dados em um formato com suporte do aplicativo servidor ou o tópico System, que fornece informações sobre o próprio aplicativo servidor.</span><span class="sxs-lookup"><span data-stu-id="5999f-115">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="5999f-116">Depois de uma conversação iniciada em um tópico específico, somente um item de dados associado àquele tópico pode ser transferido.</span><span class="sxs-lookup"><span data-stu-id="5999f-116">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>
>>>>>>> <span data-ttu-id="5999f-117">mestre</span><span class="sxs-lookup"><span data-stu-id="5999f-117">master</span></span>

<span data-ttu-id="5999f-p103">Por exemplo, suponha que você esteja executando o Microsoft Word e queira inserir dados de um banco de dados específico do Microsoft Access em um documento. Comece uma conversação DDE com o Microsoft Access abrindo um canal DDE com a função **DDEInitiate** e especificando o nome do arquivo de banco de dados como o tópico. Em seguida, será transferir os dados daquele banco de dados para o Microsoft Word por meio desse canal.</span><span class="sxs-lookup"><span data-stu-id="5999f-p103">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document. You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic. You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="5999f-121">Como um servidor DDE, o Microsoft Access dá suporte a estes tópicos:</span><span class="sxs-lookup"><span data-stu-id="5999f-121">As a DDE server, Microsoft Access supports the following topics:</span></span>

<span data-ttu-id="5999f-122"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5999f-122"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="5999f-123">O tópico System</span><span class="sxs-lookup"><span data-stu-id="5999f-123">The System topic</span></span>

  - <span data-ttu-id="5999f-124">O nome de um banco de dados (tópico *database*)</span><span class="sxs-lookup"><span data-stu-id="5999f-124">The name of a database (*database* topic)</span></span>

  - <span data-ttu-id="5999f-125">O nome de uma tabela (tópico *tablename*)</span><span class="sxs-lookup"><span data-stu-id="5999f-125">The name of a table (*tablename* topic)</span></span>

  - <span data-ttu-id="5999f-126">O nome de uma consulta (tópico *queryname*)</span><span class="sxs-lookup"><span data-stu-id="5999f-126">The name of a query (*queryname* topic)</span></span>

  - <span data-ttu-id="5999f-127">Uma cadeia SQL do Microsoft Access (tópico *sqlstring*)</span><span class="sxs-lookup"><span data-stu-id="5999f-127">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="5999f-p104">Uma vez estabelecida uma conversação DDE, use a instrução **DDEExecute** para enviar um comando do aplicativo cliente para o aplicativo servidor. Quando usado como um servidor DDE, o Microsoft Access reconhece qualquer um destes como comandos válidos:</span><span class="sxs-lookup"><span data-stu-id="5999f-p104">Once you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application. When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

  - <span data-ttu-id="5999f-130">O nome de uma macro no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="5999f-130">The name of a macro in the current database.</span></span>

  - <span data-ttu-id="5999f-131">Qualquer ação executável no Visual Basic através de um dos métodos do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="5999f-131">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

  - <span data-ttu-id="5999f-p105">As ações AbrirBancoDeDados e FecharBancoDeDados, usadas somente para operações DDE. (Um exemplo de como usar essas ações encontra-se adiante neste tópico).</span><span class="sxs-lookup"><span data-stu-id="5999f-p105">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>


> [!NOTE]
> <P><span data-ttu-id="5999f-p106">[!OBSERVAçãO] Quando você especifica uma ação de macro como uma instrução <STRONG>DDEExecute</STRONG>, a ação e quaisquer argumentos seguem a sintaxe do objeto <STRONG>DoCmd</STRONG> e precisam vir entre colchetes ([ ]). No entanto, aplicativos que dão suporte à DDE não reconhecem constantes intrínsecas em operações DDE. Além disso, argumentos de cadeias de caracteres precisam vir entre aspas (" ") se a cadeia contiver uma vírgula. Senão, as aspas são desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="5999f-p106">When you specify a macro action as a <STRONG>DDEExecute</STRONG> statement, the action and any arguments follow the <STRONG>DoCmd</STRONG> object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span></P>



<span data-ttu-id="5999f-p107">O aplicativo cliente pode usar a função **DDERequest** para solicitar dados de texto do aplicativo servidor através de um canal DDE aberto. Outra alternativa é o cliente usar a instrução **DDEPoke** para enviar dados ao aplicativo servidor. Assim que a transferência de dados for concluída, o cliente poderá usar a instrução **DDETerminate** para fechar o canal DDE ou a instrução **DDETerminateAll** para fechar todos os canais abertos.</span><span class="sxs-lookup"><span data-stu-id="5999f-p107">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel. Or the client can use the **DDEPoke** statement to send data to the server application. Once the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5999f-141">[!OBSERVAçãO] Quando o aplicativo cliente termina de receber dados através de um canal DDE, deve fechar aquele canal para poupar recursos de memória.</span><span class="sxs-lookup"><span data-stu-id="5999f-141">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span></P>


=======
- <span data-ttu-id="5999f-142">O tópico System</span><span class="sxs-lookup"><span data-stu-id="5999f-142">The System topic</span></span>

- <span data-ttu-id="5999f-143">O nome de um banco de dados (tópico *database*)</span><span class="sxs-lookup"><span data-stu-id="5999f-143">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="5999f-144">O nome de uma tabela (tópico *tablename*)</span><span class="sxs-lookup"><span data-stu-id="5999f-144">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="5999f-145">O nome de uma consulta (tópico *queryname*)</span><span class="sxs-lookup"><span data-stu-id="5999f-145">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="5999f-146">Uma cadeia SQL do Microsoft Access (tópico *sqlstring*)</span><span class="sxs-lookup"><span data-stu-id="5999f-146">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="5999f-147">Depois que você estabelecer uma conversação DDE, você pode usar a instrução **DDEExecute** para enviar um comando do cliente para o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="5999f-147">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="5999f-148">Quando usado como um servidor DDE, o Microsoft Access reconhece qualquer um destes como comandos válidos:</span><span class="sxs-lookup"><span data-stu-id="5999f-148">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="5999f-149">O nome de uma macro no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="5999f-149">The name of a macro in the current database.</span></span>

- <span data-ttu-id="5999f-150">Qualquer ação executável no Visual Basic através de um dos métodos do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="5999f-150">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="5999f-p109">As ações AbrirBancoDeDados e FecharBancoDeDados, usadas somente para operações DDE. (Um exemplo de como usar essas ações encontra-se adiante neste tópico).</span><span class="sxs-lookup"><span data-stu-id="5999f-p109">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="5999f-p110">[!OBSERVAçãO] Quando você especifica uma ação de macro como uma instrução **DDEExecute**, a ação e quaisquer argumentos seguem a sintaxe do objeto **DoCmd** e precisam vir entre colchetes ([ ]). No entanto, aplicativos que dão suporte à DDE não reconhecem constantes intrínsecas em operações DDE. Além disso, argumentos de cadeias de caracteres precisam vir entre aspas (" ") se a cadeia contiver uma vírgula. Senão, as aspas são desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="5999f-p110">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="5999f-157">O aplicativo cliente pode usar a função **DDERequest** para solicitar dados de texto do aplicativo servidor através de um canal DDE aberto.</span><span class="sxs-lookup"><span data-stu-id="5999f-157">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="5999f-158">Outra alternativa é o cliente usar a instrução **DDEPoke** para enviar dados ao aplicativo servidor.</span><span class="sxs-lookup"><span data-stu-id="5999f-158">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="5999f-159">Quando a transferência de dados for concluída, o cliente pode usar a instrução **DDETerminate** para fechar o canal DDE ou a instrução **DDETerminateAll** para fechar todos os canais abertos.</span><span class="sxs-lookup"><span data-stu-id="5999f-159">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="5999f-160">[!OBSERVAçãO] Quando o aplicativo cliente termina de receber dados através de um canal DDE, deve fechar aquele canal para poupar recursos de memória.</span><span class="sxs-lookup"><span data-stu-id="5999f-160">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>
>>>>>>> <span data-ttu-id="5999f-161">mestre</span><span class="sxs-lookup"><span data-stu-id="5999f-161">master</span></span>

<span data-ttu-id="5999f-p112">O exemplo a seguir demonstra como criar um procedimento do Microsoft Word com Visual Basic que usa o Microsoft Access como um servidor DDE. (Para este exemplo funcionar, o Microsoft Access deve estar sendo executado).</span><span class="sxs-lookup"><span data-stu-id="5999f-p112">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server. (For this example to work, Microsoft Access must be running.)</span></span>

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

<a name="-head"></a><span data-ttu-id="5999f-164"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5999f-164"><<<<<<< HEAD</span></span>
=======
<br/>

>>>>>>> <span data-ttu-id="5999f-165">As seções a seguir fornecem informações sobre os tópicos DDE válidos com suporte pelo Microsoft Access de mestre.</span><span class="sxs-lookup"><span data-stu-id="5999f-165">master The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="5999f-166">O tópico System</span><span class="sxs-lookup"><span data-stu-id="5999f-166">The System topic</span></span>

<span data-ttu-id="5999f-167"><<<<<<< Tópico cabeça o sistema é um tópico padrão para todos os aplicativos Microsoft baseada no Windows.</span><span class="sxs-lookup"><span data-stu-id="5999f-167"><<<<<<< HEAD The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="5999f-168">Ele fornece informações sobre os outros tópicos com suporte do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5999f-168">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="5999f-169">Para acessar essa informação, seu código deve primeiro chamar a função **DDEInitiate** com como o argumento *topic* e executar a instrução **DDERequest** com um dos seguintes fornecidos para o argumento *item* .</span><span class="sxs-lookup"><span data-stu-id="5999f-169">To access this information, your code must first call the **DDEInitiate** function with as the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>
<span data-ttu-id="5999f-170">=== O tópico System é um tópico padrão para todos os aplicativos Microsoft baseada no Windows.</span><span class="sxs-lookup"><span data-stu-id="5999f-170">======= The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="5999f-171">Ele fornece informações sobre os outros tópicos com suporte do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5999f-171">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="5999f-172">Para acessar essa informação, seu código deve primeiro chamar a função **DDEInitiate** com o argumento *topic* e executar a instrução **DDERequest** com um dos seguintes fornecidos para o argumento *item* .</span><span class="sxs-lookup"><span data-stu-id="5999f-172">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>
>>>>>>> <span data-ttu-id="5999f-173">mestre</span><span class="sxs-lookup"><span data-stu-id="5999f-173">master</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5999f-174">Item</span><span class="sxs-lookup"><span data-stu-id="5999f-174">Item</span></span></p></th>
<th><p><span data-ttu-id="5999f-175">Retornos</span><span class="sxs-lookup"><span data-stu-id="5999f-175">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5999f-176">SysItems</span><span class="sxs-lookup"><span data-stu-id="5999f-176">SysItems</span></span></p></td>
<td><p><span data-ttu-id="5999f-177">Uma lista de itens com suporte do tópico Sistema no Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5999f-177">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-178">Formats</span><span class="sxs-lookup"><span data-stu-id="5999f-178">Formats</span></span></p></td>
<td><p><span data-ttu-id="5999f-179">Uma lista dos formatos que o Microsoft Access consegue copiar para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="5999f-179">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-180">Status</span><span class="sxs-lookup"><span data-stu-id="5999f-180">Status</span></span></p></td>
<td><p><span data-ttu-id="5999f-181">&quot;Ocupado&quot; ou &quot;pronto&quot;.</span><span class="sxs-lookup"><span data-stu-id="5999f-181">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-182">Topics</span><span class="sxs-lookup"><span data-stu-id="5999f-182">Topics</span></span></p></td>
<td><p><span data-ttu-id="5999f-183">Uma lista de todos os bancos de dados abertos.</span><span class="sxs-lookup"><span data-stu-id="5999f-183">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="5999f-184"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5999f-184"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="5999f-185">mestre</span><span class="sxs-lookup"><span data-stu-id="5999f-185">master</span></span>

<span data-ttu-id="5999f-186">O exemplo a seguir demonstra o uso das funções **DDEInitiate** e **DDERequest** com o tópico System:</span><span class="sxs-lookup"><span data-stu-id="5999f-186">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

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

## <a name="the-database-topic"></a><span data-ttu-id="5999f-187">O tópico de banco de dados</span><span class="sxs-lookup"><span data-stu-id="5999f-187">The database topic</span></span>

<span data-ttu-id="5999f-188">O tópico de *banco de dados* é o nome de arquivo do banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="5999f-188">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="5999f-189">É possível digitar apenas o nome básico (Northwind) ou seu caminho e extensão. mdb (c:\\acesso\\amostras\\Northwind. mdb).</span><span class="sxs-lookup"><span data-stu-id="5999f-189">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="5999f-190">Após iniciar uma conversação DDE com o banco de dados, você pode solicitar uma lista dos objetos naquele banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5999f-190">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

<span data-ttu-id="5999f-191"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5999f-191"><<<<<<< HEAD</span></span>

> [!NOTE]
> <P><span data-ttu-id="5999f-192">[!OBSERVAçãO] Não é possível usar a DDE para consultar o arquivo de informações do grupo de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5999f-192">You can't use DDE to query the Microsoft Access workgroup information file.</span></span></P>


=======
> [!NOTE]
> <span data-ttu-id="5999f-193">[!OBSERVAçãO] Não é possível usar a DDE para consultar o arquivo de informações do grupo de trabalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5999f-193">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>
>>>>>>> <span data-ttu-id="5999f-194">mestre</span><span class="sxs-lookup"><span data-stu-id="5999f-194">master</span></span>

<span data-ttu-id="5999f-195">O tópico *database* oferece suporte aos seguintes itens.</span><span class="sxs-lookup"><span data-stu-id="5999f-195">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5999f-196">Item</span><span class="sxs-lookup"><span data-stu-id="5999f-196">Item</span></span></p></th>
<th><p><span data-ttu-id="5999f-197">Retornos</span><span class="sxs-lookup"><span data-stu-id="5999f-197">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5999f-198">TableList</span><span class="sxs-lookup"><span data-stu-id="5999f-198">TableList</span></span></p></td>
<span data-ttu-id="5999f-199"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5999f-199"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="5999f-200">Uma lista de tabelas.</span><span class="sxs-lookup"><span data-stu-id="5999f-200">A list of tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-201">QueryList</span><span class="sxs-lookup"><span data-stu-id="5999f-201">QueryList</span></span></p></td>
<td><p><span data-ttu-id="5999f-202">Uma lista de consultas.</span><span class="sxs-lookup"><span data-stu-id="5999f-202">A list of queries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-203">FormList</span><span class="sxs-lookup"><span data-stu-id="5999f-203">FormList</span></span></p></td>
<td><p><span data-ttu-id="5999f-204">Uma lista de formulários.</span><span class="sxs-lookup"><span data-stu-id="5999f-204">A list of forms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-205">ReportList</span><span class="sxs-lookup"><span data-stu-id="5999f-205">ReportList</span></span></p></td>
<td><p><span data-ttu-id="5999f-206">Uma lista de relatórios.</span><span class="sxs-lookup"><span data-stu-id="5999f-206">A list of reports.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-207">MacroList</span><span class="sxs-lookup"><span data-stu-id="5999f-207">MacroList</span></span></p></td>
<td><p><span data-ttu-id="5999f-208">Uma lista de macros.</span><span class="sxs-lookup"><span data-stu-id="5999f-208">A list of macros.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-209">ModuleList</span><span class="sxs-lookup"><span data-stu-id="5999f-209">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="5999f-210">Uma lista de módulos.</span><span class="sxs-lookup"><span data-stu-id="5999f-210">A list of modules.</span></span></p></td>
=======
<td><p><span data-ttu-id="5999f-211">Uma lista de tabelas</span><span class="sxs-lookup"><span data-stu-id="5999f-211">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-212">QueryList</span><span class="sxs-lookup"><span data-stu-id="5999f-212">QueryList</span></span></p></td>
<td><p><span data-ttu-id="5999f-213">Uma lista de consultas</span><span class="sxs-lookup"><span data-stu-id="5999f-213">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-214">FormList</span><span class="sxs-lookup"><span data-stu-id="5999f-214">FormList</span></span></p></td>
<td><p><span data-ttu-id="5999f-215">Uma lista de formulários</span><span class="sxs-lookup"><span data-stu-id="5999f-215">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-216">ReportList</span><span class="sxs-lookup"><span data-stu-id="5999f-216">ReportList</span></span></p></td>
<td><p><span data-ttu-id="5999f-217">Uma lista de relatórios</span><span class="sxs-lookup"><span data-stu-id="5999f-217">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-218">MacroList</span><span class="sxs-lookup"><span data-stu-id="5999f-218">MacroList</span></span></p></td>
<td><p><span data-ttu-id="5999f-219">Uma lista de macros</span><span class="sxs-lookup"><span data-stu-id="5999f-219">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-220">ModuleList</span><span class="sxs-lookup"><span data-stu-id="5999f-220">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="5999f-221">Uma lista dos módulos</span><span class="sxs-lookup"><span data-stu-id="5999f-221">A list of modules</span></span></p></td><span data-ttu-id="5999f-222">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="5999f-222">
>>>>>>> master</span></span>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-223">ViewList</span><span class="sxs-lookup"><span data-stu-id="5999f-223">ViewList</span></span></p></td>
<td><p><span data-ttu-id="5999f-224">Uma lista de modos.</span><span class="sxs-lookup"><span data-stu-id="5999f-224">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-225">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="5999f-225">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="5999f-226">Uma lista de procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="5999f-226">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-227">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="5999f-227">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="5999f-228">Uma lista de diagramas de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="5999f-228">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="5999f-229"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5999f-229"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="5999f-230">mestre</span><span class="sxs-lookup"><span data-stu-id="5999f-230">master</span></span>

<span data-ttu-id="5999f-231">O exemplo a seguir mostra como abrir o formulário Employees no exemplo de banco de dados Northwind a partir de um procedimento do Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5999f-231">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

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

## <a name="the-table-topic"></a><span data-ttu-id="5999f-232">O tópico de tabela</span><span class="sxs-lookup"><span data-stu-id="5999f-232">The TABLE topic</span></span>

<span data-ttu-id="5999f-233">Esses tópicos usam a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="5999f-233">These topics use the following syntax:</span></span>

<span data-ttu-id="5999f-234">_databasename_ ; **Tabela** _TableName_</span><span class="sxs-lookup"><span data-stu-id="5999f-234">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="5999f-235">_databasename_ ; **Consulta** _queryname_</span><span class="sxs-lookup"><span data-stu-id="5999f-235">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="5999f-236">_databasename_ ; **SQL** [ _sqlstring_ ]</span><span class="sxs-lookup"><span data-stu-id="5999f-236">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5999f-237">Parte</span><span class="sxs-lookup"><span data-stu-id="5999f-237">Part</span></span></p></th>
<th><p><span data-ttu-id="5999f-238">Descrição</span><span class="sxs-lookup"><span data-stu-id="5999f-238">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5999f-239"><em>databasename</em></span><span class="sxs-lookup"><span data-stu-id="5999f-239"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="5999f-p115">O nome do banco de dados em que está a tabela ou consulta ou a que se aplica o SQL, seguido de ponto-e-vírgula (;). O nome do banco de dados pode ser apenas o nome básico (Northwind) ou seu caminho e extensão .mdb completos (C:\Access\Exemplos\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="5999f-p115">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;). The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-242"><em>tablename</em></span><span class="sxs-lookup"><span data-stu-id="5999f-242"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="5999f-243">O nome de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="5999f-243">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-244"><em>queryname</em></span><span class="sxs-lookup"><span data-stu-id="5999f-244"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="5999f-245">O nome de uma consulta existente.</span><span class="sxs-lookup"><span data-stu-id="5999f-245">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-246"><em>sqlstring</em></span><span class="sxs-lookup"><span data-stu-id="5999f-246"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="5999f-247">Uma instrução SQL válida até 256 caracteres e terminando com um ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="5999f-247">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="5999f-248">Para trocar mais de 256 caracteres, omitir esse argumento e, em vez disso, use sucessivas instruções <strong>DDEPoke</strong> para formar uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="5999f-248">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="5999f-249">Por exemplo, o seguinte código Visual Basic utiliza a instrução <strong>DDEPoke</strong> para formar uma instrução SQL e, em seguida, solicitar os resultados de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="5999f-249">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="5999f-250">A tabela a seguir lista os itens válidos para os tópicos TABELA *tablename*, CONSULTA *queryname* e SQL *sqlstring*.</span><span class="sxs-lookup"><span data-stu-id="5999f-250">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5999f-251">Item</span><span class="sxs-lookup"><span data-stu-id="5999f-251">Item</span></span></p></th>
<th><p><span data-ttu-id="5999f-252">Retornos</span><span class="sxs-lookup"><span data-stu-id="5999f-252">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5999f-253">All</span><span class="sxs-lookup"><span data-stu-id="5999f-253">All</span></span></p></td>
<td><p><span data-ttu-id="5999f-254">Todos os dados na tabela, incluindo nomes de campos.</span><span class="sxs-lookup"><span data-stu-id="5999f-254">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-255">Data</span><span class="sxs-lookup"><span data-stu-id="5999f-255">Data</span></span></p></td>
<td><p><span data-ttu-id="5999f-256">Todas as linhas de dados, sem nomes de campos.</span><span class="sxs-lookup"><span data-stu-id="5999f-256">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-257">FieldNames</span><span class="sxs-lookup"><span data-stu-id="5999f-257">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="5999f-258">Uma lista de linha única de nomes de campos.</span><span class="sxs-lookup"><span data-stu-id="5999f-258">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-259">FieldNames; T</span><span class="sxs-lookup"><span data-stu-id="5999f-259">FieldNames;T</span></span></p></td>
<span data-ttu-id="5999f-260"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5999f-260"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="5999f-261">Uma lista de duas linhas de nomes de campos (primeira linha) e seus tipos de dados (segunda linha).</span><span class="sxs-lookup"><span data-stu-id="5999f-261">A two-row list of field names (first row) and their data types (second row).</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-262">Estes são os valores retornados e os tipos de dados que representam:</span><span class="sxs-lookup"><span data-stu-id="5999f-262">These are the values returned and the data types they represent:</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-263"><b>Valor</b></span><span class="sxs-lookup"><span data-stu-id="5999f-263"><b>Value</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-264">0</span><span class="sxs-lookup"><span data-stu-id="5999f-264">0</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-265">1</span><span class="sxs-lookup"><span data-stu-id="5999f-265">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-266">2</span><span class="sxs-lookup"><span data-stu-id="5999f-266">2</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-267">3</span><span class="sxs-lookup"><span data-stu-id="5999f-267">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-268">4</span><span class="sxs-lookup"><span data-stu-id="5999f-268">4</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-269">5</span><span class="sxs-lookup"><span data-stu-id="5999f-269">5</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-270">6</span><span class="sxs-lookup"><span data-stu-id="5999f-270">6</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-271">7</span><span class="sxs-lookup"><span data-stu-id="5999f-271">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-272">8</span><span class="sxs-lookup"><span data-stu-id="5999f-272">8</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-273">9</span><span class="sxs-lookup"><span data-stu-id="5999f-273">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-274">10</span><span class="sxs-lookup"><span data-stu-id="5999f-274">10</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-275">11</span><span class="sxs-lookup"><span data-stu-id="5999f-275">11</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5999f-276">12</span><span class="sxs-lookup"><span data-stu-id="5999f-276">12</span></span></p></td>
=======
<td><p><span data-ttu-id="5999f-277">Uma lista de duas linhas de nomes de campos (primeira linha) e seus tipos de dados (segunda linha).</span><span class="sxs-lookup"><span data-stu-id="5999f-277">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="5999f-278">Estes são os valores retornados:</span><span class="sxs-lookup"><span data-stu-id="5999f-278">These are the values returned:</span></span></p>
<p><span data-ttu-id="5999f-279">Valor</span><span class="sxs-lookup"><span data-stu-id="5999f-279">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="5999f-280">0</span><span class="sxs-lookup"><span data-stu-id="5999f-280">0</span></span></li>
<li><span data-ttu-id="5999f-281">1</span><span class="sxs-lookup"><span data-stu-id="5999f-281">1</span></span></li>
<li><span data-ttu-id="5999f-282">2</span><span class="sxs-lookup"><span data-stu-id="5999f-282">2</span></span></li>
<li><span data-ttu-id="5999f-283">3</span><span class="sxs-lookup"><span data-stu-id="5999f-283">3</span></span></li>
<li><span data-ttu-id="5999f-284">4</span><span class="sxs-lookup"><span data-stu-id="5999f-284">4</span></span></li>
<li><span data-ttu-id="5999f-285">5</span><span class="sxs-lookup"><span data-stu-id="5999f-285">5</span></span></li>
<li><span data-ttu-id="5999f-286">6</span><span class="sxs-lookup"><span data-stu-id="5999f-286">6</span></span></li>
<li><span data-ttu-id="5999f-287">7</span><span class="sxs-lookup"><span data-stu-id="5999f-287">7</span></span></li>
<li><span data-ttu-id="5999f-288">8</span><span class="sxs-lookup"><span data-stu-id="5999f-288">8</span></span></li>
<li><span data-ttu-id="5999f-289">9</span><span class="sxs-lookup"><span data-stu-id="5999f-289">9</span></span></li>
<li><span data-ttu-id="5999f-290">10</span><span class="sxs-lookup"><span data-stu-id="5999f-290">10</span></span></li>
<li><span data-ttu-id="5999f-291">11</span><span class="sxs-lookup"><span data-stu-id="5999f-291">11</span></span></li>
<li><span data-ttu-id="5999f-292">12</span><span class="sxs-lookup"><span data-stu-id="5999f-292">12</span></span></li>
</ul>
</p>
</td><span data-ttu-id="5999f-293">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="5999f-293">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-294">NextRow</span><span class="sxs-lookup"><span data-stu-id="5999f-294">NextRow</span></span></p></td>
<td><p><span data-ttu-id="5999f-p117">Os dados na próxima linha da tabela ou consulta. Quando você abre um canal, NextRow retorna os dados da primeira linha. Se a linha atual for o último registro e você executar NextRow, a solicitação falhará.</span><span class="sxs-lookup"><span data-stu-id="5999f-p117">The data in the next row in the table or query. When you open a channel, NextRow returns the data in the first row. If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-298">PrevRow</span><span class="sxs-lookup"><span data-stu-id="5999f-298">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="5999f-p118">Os dados na linha anterior da tabela ou consulta. Se PrevRow for a primeira solicitação em um novo canal, os dados na última linha da tabela ou consulta serão retornados. Se o primeiro registro for a linha atual, a solicitação a PrevRow falhará.</span><span class="sxs-lookup"><span data-stu-id="5999f-p118">The data in the previous row in the table or query. If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned. If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-302">FirstRow</span><span class="sxs-lookup"><span data-stu-id="5999f-302">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="5999f-303">Os dados na primeira linha da tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="5999f-303">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-304">LastRow</span><span class="sxs-lookup"><span data-stu-id="5999f-304">LastRow</span></span></p></td>
<td><p><span data-ttu-id="5999f-305">Os dados na última linha da tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="5999f-305">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-306">FieldCount</span><span class="sxs-lookup"><span data-stu-id="5999f-306">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="5999f-307">O número de campos na tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="5999f-307">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5999f-308">SQLText</span><span class="sxs-lookup"><span data-stu-id="5999f-308">SQLText</span></span></p></td>
<td><p><span data-ttu-id="5999f-309">Uma instrução SQL que representa a tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="5999f-309">An SQL statement representing the table or query.</span></span> <span data-ttu-id="5999f-310">Para tabelas, esse item retorna uma instrução SQL no formato &quot;selecione `*` da <em>tabela</em>; &quot;.</span><span class="sxs-lookup"><span data-stu-id="5999f-310">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5999f-311">SQLText;<em>n</em></span><span class="sxs-lookup"><span data-stu-id="5999f-311">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="5999f-312">Uma instrução SQL, em que <em>n</em>-partes, representando a tabela ou consulta, onde <em>n</em> é um inteiro de até 256 de caractere.</span><span class="sxs-lookup"><span data-stu-id="5999f-312">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="5999f-313">Por exemplo, suponhamos que uma consulta é representada pela seguinte instrução SQL: O item &quot;SQLText; 7&quot; retorna os seguintes blocos de delimitado por tabulação: O item &quot;SQLText; 7&quot; retorna os seguintes blocos de delimitado por tabulações:</span><span class="sxs-lookup"><span data-stu-id="5999f-313">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><span data-ttu-id="5999f-314"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="5999f-314"><<<<<<< HEAD</span></span>
=======
<br/>
>>>>>>> <span data-ttu-id="5999f-315">mestre</span><span class="sxs-lookup"><span data-stu-id="5999f-315">master</span></span>

<span data-ttu-id="5999f-316">O exemplo a seguir mostra como usar DDE em um procedimento do Visual Basic para solicitar dados de uma tabela no exemplo de banco de dados Northwind e inserir os dados em um arquivo de texto:</span><span class="sxs-lookup"><span data-stu-id="5999f-316">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

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
