---
title: 'Capítulo 12: Tutorial do Remote Data Service (RDS)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704802"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a><span data-ttu-id="08f4b-102">Capítulo 12: Tutorial do Remote Data Service (RDS)</span><span class="sxs-lookup"><span data-stu-id="08f4b-102">Chapter 12: Remote Data Service (RDS) tutorial</span></span>

<span data-ttu-id="08f4b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="08f4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08f4b-104">Este tutorial ilustra o uso do modelo de programação RDS para consultar e atualizar uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="08f4b-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="08f4b-105">Primeiramente, ele descreve as etapas necessárias para realizar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="08f4b-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="08f4b-106">Em seguida, o tutorial é repetido no Microsoft Visual Basic Scripting Edition e Microsoft Visual J++, apresentando o ADO for Windows Foundation Classes (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="08f4b-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="08f4b-107">Este tutorial é codificado em diferentes linguagens por dois motivos:</span><span class="sxs-lookup"><span data-stu-id="08f4b-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="08f4b-p102">A documentação do RDS assume os códigos do leitor no Visual Basic. Isso torna a documentação conveniente para programadores do Visual Basic, mas menos útil para os programadores que utilizam outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="08f4b-110">Se você não estiver certo quanto a um determinado recurso RDS e conhecer um pouco de outra linguagem, pode conseguir resolver sua questão para o mesmo recurso expresso em outra linguagem.</span><span class="sxs-lookup"><span data-stu-id="08f4b-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

<span data-ttu-id="08f4b-p103">Esse tutorial é baseado no modelo de programação RDS. Ele discute cada etapa do modelo de programação individualmente. Além disso, ilustra cada etapa com um fragmento do código do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="08f4b-p104">O exemplo do código é repetido em outras linguagens com a discussão mínima. Cada etapa em um determinado tutorial de linguagem de programação está marcado com a etapa correspondente no modelo de programação e tutorial descritivo. Utilize o número da etapa para se referir à discussão no tutorial descritivo.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="08f4b-p105">O modelo de programação RDS está indicado abaixo. Utilize-o como um roteiro conforme avança no tutorial.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

### <a name="rds-programming-model-with-objects"></a><span data-ttu-id="08f4b-119">Modelo de programação do RDS com objetos</span><span class="sxs-lookup"><span data-stu-id="08f4b-119">RDS programming model with objects</span></span>

- <span data-ttu-id="08f4b-120">Especifique o programa a ser chamado no servidor e obtenha uma maneira (proxy) de se referir a ele a partir do cliente.</span><span class="sxs-lookup"><span data-stu-id="08f4b-120">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="08f4b-p106">Chame o programa do servidor. Transmita os parâmetros ao programa do servidor que identifica a fonte de dados e o comando a ser emitido.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="08f4b-p107">O programa do servidor obtém um objeto [Recordset](recordset-object-ado.md) da fonte de dados, geralmente usando o ADO. Opcionalmente, o objeto **Recordset** é processado no servidor.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="08f4b-125">O programa do servidor retorna o objeto **Recordset** final ao aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="08f4b-125">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="08f4b-126">No cliente, o objeto **Recordset** é colocado opcionalmente em um formulário que pode ser facilmente usado por controle visuais.</span><span class="sxs-lookup"><span data-stu-id="08f4b-126">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="08f4b-127">As alterações ao objeto **Recordset** são enviadas de volta ao servidor e utilizadas para atualizar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="08f4b-127">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

## <a name="step-1-specify-a-server-program"></a><span data-ttu-id="08f4b-128">Etapa 1: Especificar um programa de servidor</span><span class="sxs-lookup"><span data-stu-id="08f4b-128">Step 1: Specify a server program</span></span>

<span data-ttu-id="08f4b-p108">No caso mais geral, use o objeto [RDS.DataSpace](dataspace-object-rds.md) do método [CreateObject](createobject-method-rds.md) para especificar o programa do servidor padrão, [RDSServer.DataFactory](datafactory-object-rdsserver.md), ou seu próprio programa de servidor personalizado (objeto de negócios). Um programa de servidor é instanciado no servidor e uma referência ao programa do servidor, ou *proxy*, é retornada.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p108">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object). A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="08f4b-131">Este tutorial usa o programa do servidor padrão:</span><span class="sxs-lookup"><span data-stu-id="08f4b-131">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a><span data-ttu-id="08f4b-132">Etapa 2: Chamar o programa do servidor</span><span class="sxs-lookup"><span data-stu-id="08f4b-132">Step 2: Invoke the server program</span></span> 

<span data-ttu-id="08f4b-p109">Ao chamar um método no *proxy* do cliente, o programa real no servidor executa o método. Nessa etapa, você executará uma consulta no servidor.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p109">When you invoke a method on the client *proxy*, the actual program on the server executes the method. In this step, you'll execute a query on the server.</span></span>

### <a name="part-a"></a><span data-ttu-id="08f4b-135">Parte A</span><span class="sxs-lookup"><span data-stu-id="08f4b-135">Part A</span></span>

<span data-ttu-id="08f4b-136">Se você não estava usando [Rdsserver](datafactory-object-rdsserver.md) neste tutorial, a maneira mais conveniente executar esta etapa seria usar o [RDS. DataControl](datacontrol-object-rds.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="08f4b-136">If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="08f4b-137">O **RDS.DataControl** combina a etapa anterior da criação de um proxy, com essa etapa, emitindo a consulta.</span><span class="sxs-lookup"><span data-stu-id="08f4b-137">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

1. <span data-ttu-id="08f4b-138">Definir o **RDS. DataControl** objeto de propriedade de [servidor](server-property-rds.md) para identificar onde o programa do servidor deve ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="08f4b-138">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated.</span></span>

2. <span data-ttu-id="08f4b-139">Defina a propriedade [Connect](connect-property-rds.md) para especificar a cadeia de caracteres de conectar para acessar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="08f4b-139">Set the [Connect](connect-property-rds.md) property to specify the connect string to access the data source.</span></span>

3. <span data-ttu-id="08f4b-140">Defina a propriedade [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) para especificar o texto de comando da consulta.</span><span class="sxs-lookup"><span data-stu-id="08f4b-140">Set the [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property to specify the query command text.</span></span> 

4. <span data-ttu-id="08f4b-141">Emitir o método [Refresh](refresh-method-rds.md) para fazer com que o programa de servidor para se conectar à fonte de dados, recuperar linhas especificadas pela consulta e retornar um objeto **Recordset** para o cliente.</span><span class="sxs-lookup"><span data-stu-id="08f4b-141">Issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="08f4b-142">Este tutorial não usa o **RDS.DataControl**, mas veja como seria se o fizesse:</span><span class="sxs-lookup"><span data-stu-id="08f4b-142">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

<span data-ttu-id="08f4b-143">Ele também não invoca RDS com objetos ADO, mas veja como seria se o fizesse:</span><span class="sxs-lookup"><span data-stu-id="08f4b-143">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a><span data-ttu-id="08f4b-144">Parte B</span><span class="sxs-lookup"><span data-stu-id="08f4b-144">Part B</span></span>

<span data-ttu-id="08f4b-145">O método geral para realizar esta etapa é invocar o método [Query](query-method-rds.md) do objeto **Rdsserver** .</span><span class="sxs-lookup"><span data-stu-id="08f4b-145">The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="08f4b-146">Esse método assume uma cadeia de conexão, que é usada para se conectar a uma origem de dados e um texto de comando, que é usada para especificar as linhas a serem retornadas a partir da origem de dados.</span><span class="sxs-lookup"><span data-stu-id="08f4b-146">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="08f4b-147">Este tutorial usa o método **Query** do objeto **DataFactory**:</span><span class="sxs-lookup"><span data-stu-id="08f4b-147">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a><span data-ttu-id="08f4b-148">Etapa 3: O servidor obtém um Recordset</span><span class="sxs-lookup"><span data-stu-id="08f4b-148">Step 3: Server obtains a Recordset</span></span> 

<span data-ttu-id="08f4b-p112">O programa do servidor usa a sequência de conexão e o texto de comando para consultar a fonte de dados para as linhas desejadas. O ADO geralmente é usado para recuperar esse **Recordset**, embora outras interfaces de acesso a dados da Microsoft, como o OLE DB, podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p112">The server program uses the connect string and command text to query the data source for the desired rows. ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="08f4b-151">Um programa de servidor personalizado pode parecer com:</span><span class="sxs-lookup"><span data-stu-id="08f4b-151">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="08f4b-152">Etapa 4: Servidor retorna o Recordset</span><span class="sxs-lookup"><span data-stu-id="08f4b-152">Step 4: Server returns the Recordset</span></span> 

<span data-ttu-id="08f4b-p113">O RDS converte o objeto **Recordset** recuperado para um formato que pode ser enviado de volta ao cliente (ou seja, ele *empacota* o **Recordset**). O formato exato da conversão e como ele é gasto depende de o servidor estar na Internet ou na intranet, uma rede local ou é uma biblioteca de vínculos dinâmicos. Contudo, este detalhe não é crítico; o que importa é que o RDS envia o **Recordset** de volta ao cliente.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p113">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**). The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library. However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="08f4b-156">No lado cliente, um objeto **Recordset** é retornado e atribuído a uma variável local.</span><span class="sxs-lookup"><span data-stu-id="08f4b-156">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a><span data-ttu-id="08f4b-157">Etapa 5: DataControl torna-se disponível</span><span class="sxs-lookup"><span data-stu-id="08f4b-157">Step 5: DataControl is made usable</span></span> 

<span data-ttu-id="08f4b-p114">O objeto **Recordset** retornado está disponível para uso. Você pode examinar, navegar ou editá-lo como faria com qualquer outro **Recordset**. As possibilidades de uso do **Recordset** dependem do seu ambiente. O Visual Basic e o Visual C++ possuem controles visuais que podem utilizar um **Recordset** diretamente ou indiretamente com a ajuda de um controle de dados de ativação.</span><span class="sxs-lookup"><span data-stu-id="08f4b-p114">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="08f4b-162">Por exemplo, se você está exibindo uma página da Web no Internet Explorer, você deseja exibir os dados do objeto **Recordset** em um controle visual.</span><span class="sxs-lookup"><span data-stu-id="08f4b-162">For example, if you are displaying a webpage in Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="08f4b-163">Controles visuais em uma página da Web não podem acessar um objeto **Recordset** diretamente.</span><span class="sxs-lookup"><span data-stu-id="08f4b-163">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="08f4b-164">No entanto, podem acessar o objeto **Recordset** através do [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="08f4b-164">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="08f4b-165">O **RDS.DataControl** torna-se utilizável por um controle visual quando sua propriedade [SourceRecordset](recordset-sourcerecordset-properties-rds.md) for definida como o objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="08f4b-165">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="08f4b-166">O objeto de controle visual deve ter seu parâmetro **DATASRC** definido como **RDS.DataControl** e sua propriedade **DATAFLD** definida como um campo de objeto **Recordset** (coluna).</span><span class="sxs-lookup"><span data-stu-id="08f4b-166">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="08f4b-167">Nesse tutorial, defina a propriedade **SourceRecordset**:</span><span class="sxs-lookup"><span data-stu-id="08f4b-167">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a><span data-ttu-id="08f4b-168">Etapa 6: As alterações são enviadas ao servidor</span><span class="sxs-lookup"><span data-stu-id="08f4b-168">Step 6: Changes are sent to the server</span></span>

<span data-ttu-id="08f4b-169">Se o objeto **Recordset** for editado, todas as alterações (ou seja, linhas que são incluídas, alteradas ou excluídas) poderão ser enviadas de volta ao servidor.</span><span class="sxs-lookup"><span data-stu-id="08f4b-169">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="08f4b-170">[!OBSERVAçãO] O comportamento padrão do RDS pode ser chamado implicitamente com os objetos ADO e o Microsoft OLE DB Remoting Provider.</span><span class="sxs-lookup"><span data-stu-id="08f4b-170">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="08f4b-171">Consultas podem retornar **Recordsets**e editado **Recordsets** pode atualizar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="08f4b-171">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="08f4b-172">Esse tutorial não chama o RDS com objetos ADO, mas veja como seria se o fizesse:</span><span class="sxs-lookup"><span data-stu-id="08f4b-172">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a><span data-ttu-id="08f4b-173">Parte A</span><span class="sxs-lookup"><span data-stu-id="08f4b-173">Part A</span></span>

<span data-ttu-id="08f4b-174">Supor que, nesse caso, que você usou apenas o [RDS. DataControl](datacontrol-object-rds.md) e se um objeto **Recordset** é agora associado a **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="08f4b-174">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="08f4b-175">O método [SubmitChanges](submitchanges-method-rds.md) atualiza a origem de dados com todas as alterações ao objeto **Recordset** se as propriedades [Server](server-property-rds.md) e [Connect](connect-property-rds.md) ainda estiverem definidas.</span><span class="sxs-lookup"><span data-stu-id="08f4b-175">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

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

### <a name="part-b"></a><span data-ttu-id="08f4b-176">Parte B</span><span class="sxs-lookup"><span data-stu-id="08f4b-176">Part B</span></span>

<span data-ttu-id="08f4b-177">Como alternativa, você poderia atualizar o servidor com o objeto [rdsserver. DataFactory](datafactory-object-rdsserver.md) , especificando uma conexão e um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="08f4b-177">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

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


## <a name="appendix-a-rds-tutorial-vbscript"></a><span data-ttu-id="08f4b-178">Apêndice a: tutorial do RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="08f4b-178">Appendix A: RDS tutorial (VBScript)</span></span>

<span data-ttu-id="08f4b-179">Esse é o tutorial do RDS, escrito em Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="08f4b-179">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="08f4b-180">Para obter uma descrição do objetivo deste tutorial, consulte introduction to neste tópico.</span><span class="sxs-lookup"><span data-stu-id="08f4b-180">For a description of the purpose of this tutorial, see the introduction to this topic.</span></span>

<span data-ttu-id="08f4b-181">Neste tutorial, [RDS. DataControl](datacontrol-object-rds.md) e [RDS. DataSpace](dataspace-object-rds.md) são criados no tempo de design; ou seja, eles são definidos com marcas object.</span><span class="sxs-lookup"><span data-stu-id="08f4b-181">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="08f4b-182">Como alternativa, eles podem ser criados no momento da execução com o método **Server.CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="08f4b-182">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="08f4b-183">Por exemplo, o objeto **RDS.DataControl** pode ser criado dessa forma:</span><span class="sxs-lookup"><span data-stu-id="08f4b-183">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

### <a name="step-1-specify-a-server-program"></a><span data-ttu-id="08f4b-184">Etapa 1: Especificar um programa de servidor</span><span class="sxs-lookup"><span data-stu-id="08f4b-184">Step 1: Specify a server program</span></span>

<span data-ttu-id="08f4b-185">O VBScript pode descobrir o nome do servidor web IIS que está sendo executado no acessando o método VBScript **Request. ServerVariables** disponível para Active Server Pages:</span><span class="sxs-lookup"><span data-stu-id="08f4b-185">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="08f4b-186">No entanto, para esse tutorial, use o servidor imaginário "yourServer".</span><span class="sxs-lookup"><span data-stu-id="08f4b-186">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="08f4b-p120">[!OBSERVAçãO] Preste atenção nos tipos de dados dos argumentos **ByRef**. O VBScript não permite que você especifique o tipo de variável, então, você deve sempre transmitir uma Variant. Quando HTTP for utilizado, o RDS permitirá a transmissão de uma Variant para um método que espera uma non-Variant, se você chamá-lo com o método **CreateObject** do objeto [RDS.DataSpace](createobject-method-rds.md). Ao utilizar DCOM ou um servidor em execução, corresponda os tipos de parâmetros no cliente e no servidor; caso contrário, receberá um erro "Incompatibilidade de tipo".</span><span class="sxs-lookup"><span data-stu-id="08f4b-p120">Pay attention to the data type of **ByRef** arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="08f4b-191">Etapa 2, r: de parte invocar o programa do servidor com RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="08f4b-191">Step 2, Part A: Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="08f4b-192">Esse exemplo é meramente um comentário para demonstrar que o comportamento padrão do **RDS.DataControl** destina-se a executar a consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="08f4b-192">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

<span data-ttu-id="08f4b-193">Vá para a etapa a seguir.</span><span class="sxs-lookup"><span data-stu-id="08f4b-193">Skip to the following step.</span></span>

### <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="08f4b-194">Etapa 4: Servidor retorna o Recordset</span><span class="sxs-lookup"><span data-stu-id="08f4b-194">Step 4: Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="08f4b-195">Etapa 5: DataControl torna-se disponível por controles visuais</span><span class="sxs-lookup"><span data-stu-id="08f4b-195">Step 5: DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="08f4b-196">Etapa 6, parte r: as alterações são enviadas para o servidor com RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="08f4b-196">Step 6, Part A: Changes are sent to the server with RDS.DataControl</span></span>

<span data-ttu-id="08f4b-197">Esse exemplo é meramente um comentário que demonstra como o **RDS.DataControl** executa as atualizações.</span><span class="sxs-lookup"><span data-stu-id="08f4b-197">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="08f4b-198">Etapa 6, parte b: as alterações são enviadas para o servidor com RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="08f4b-198">Step 6, Part B: Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a><span data-ttu-id="08f4b-199">Apêndice b: tutorial do RDS (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="08f4b-199">Appendix B: RDS tutorial (Visual J++)</span></span>

<span data-ttu-id="08f4b-p121">O ADO/WFC não segue completamente o modelo de objeto RDS porque não implementa o objeto [RDS.DataControl](datacontrol-object-rds.md). O ADO/WFC apenas implementa a classe do lado do cliente, [RDS.DataSpace](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="08f4b-p121">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object. ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="08f4b-p122">A classe **DataSpace** implementa um método, [CreateObject](createobject-method-rds.md), que retorna um objeto [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax). A classe **DataSpace** também implementa a propriedade [InternetTimeout](internettimeout-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="08f4b-p122">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) object. The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="08f4b-204">A classe **ObjectProxy** implementa um método, call, que pode chamar qualquer objeto de negócios do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="08f4b-204">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



