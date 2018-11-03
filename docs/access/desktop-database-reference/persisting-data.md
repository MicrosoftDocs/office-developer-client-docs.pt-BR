---
title: Mantendo dados (referência de banco de dados da área de trabalho do Access)
TOCTitle: Persisting data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d72ba6d895fc5aac2612eb3f81ecc95ac032d49
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946745"
---
# <a name="persisting-data"></a><span data-ttu-id="52aac-102">Mantendo dados</span><span class="sxs-lookup"><span data-stu-id="52aac-102">Persisting data</span></span>


<span data-ttu-id="52aac-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="52aac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52aac-p101">A computação portátil (por exemplo, a utilização de laptops) gerou a necessidade de aplicativos que possam ser executados conectados e desconectados. O ADO adicionou suporte a isso, permitindo ao desenvolvedor salvar um **Recordset** de cursor do cliente no disco e recarregá-lo posteriormente.</span><span class="sxs-lookup"><span data-stu-id="52aac-p101">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state. ADO has added support for this by giving the developer the ability to save a client cursor **Recordset** to disk and reload it later.</span></span>

<span data-ttu-id="52aac-106">Há vários cenários nos quais você poderia usar esse tipo de recurso, incluindo os seguintes:</span><span class="sxs-lookup"><span data-stu-id="52aac-106">There are several scenarios in which you could use this type of feature, including the following:</span></span>

- <span data-ttu-id="52aac-107">**Viagens:** ao levar o aplicativo em viagem, é essencial fornecer a capacidade de fazer alterações e adicionar novos registros que possam ser posteriormente reconectados ao banco de dados e confirmados.</span><span class="sxs-lookup"><span data-stu-id="52aac-107">**Traveling:** When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</span></span>

- <span data-ttu-id="52aac-p102">**Pesquisas atualizadas raramente:** Frequentemente em um aplicativo as tabelas são usadas como pesquisas  por exemplo, as tabelas de impostos estaduais. Elas são atualizadas raramente e são somente leitura. Em vez de reler esses dados do servidor cada vez que o aplicativo é iniciado, ele pode simplesmente carregar os dados de um **Recordset** mantido localmente.</span><span class="sxs-lookup"><span data-stu-id="52aac-p102">**Infrequently updated lookups:** Often in an application, tables are used as lookups — for example, state tax tables. They are infrequently updated and are read-only. Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted **Recordset**.</span></span>

<span data-ttu-id="52aac-111">No ADO, para salvar e carregar **Recordsets**, use os métodos **Recordset.Save** e **Recordset.Open(,,,,adCmdFile)** no objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="52aac-111">In ADO, to save and load **Recordsets**, use the **Recordset.Save** and **Recordset.Open(,,,,adCmdFile)** methods on the ADO **Recordset** object.</span></span>

<span data-ttu-id="52aac-p103">Você pode usar o método **Save** do **Recordset** para manter o **Recordset** do ADO em um arquivo em um disco. (Também é possível salvar um **Recordset** em um objeto **Stream** do ADO. Os objetos **Stream** são abordados posteriormente no guia.) Depois, você pode usar o método **Open** para abrir o **Recordset** novamente quando estiver pronto para usá-lo. Por padrão, o ADO salva o **Recordset** no formato Microsoft Advanced Data TableGram (ADTG) proprietário. Esse formato binário é especificado usando o valor **adPersistADTG** **PersistFormatEnum**. Alternativamente, você pode salvar seu **Recordset** fora, como XML, em vez de usar o **adPersistXML**. Para obter mais informações sobre como salvar Recordsets como XML, consulte [Mantendo registros em formato XML](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="52aac-p103">You can use the **Recordset** **Save** method to persist your ADO **Recordset** to a file on a disk. (You can also save a **Recordset** to an ADO **Stream** object. **Stream** objects are discussed later in the guide.) Later, you can use the **Open** method to reopen the **Recordset** when you are ready to use it. By default, ADO saves the **Recordset** into the proprietary Microsoft Advanced Data TableGram (ADTG) format. This binary format is specified using the **adPersistADTG** **PersistFormatEnum** value. Alternatively, you may choose to save your **Recordset** out as XML instead using **adPersistXML**. For more information about saving Recordsets as XML, see [Persisting Records in XML Format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="52aac-119">A sintaxe do método **Save** é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="52aac-119">The syntax of the **Save** method is as follows:</span></span>

`recordset.Save Destination, PersistFormat`

<span data-ttu-id="52aac-p104">Na primeira vez que você salva o **Recordset**, é opcional especificar *Destination*. Se você omitir *Destination*, será criado um novo arquivo com o nome definido como o valor da propriedade [Source](source-property-ado-recordset.md) do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="52aac-p104">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="52aac-p105">Omita *Destination* ao chamar **Save** subsequentemente após o primeiro salvamento, ou ocorrerá um erro em tempo de execução. Se você chamar **Save** subsequentemente com um novo *Destination*, o **Recordset** será salvo no novo destino. Contudo, o novo destino e o destino original serão abertos.</span><span class="sxs-lookup"><span data-stu-id="52aac-p105">Omit *Destination* when you subsequently call **Save** after the first save or a run-time error will occur. If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination. However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="52aac-p106">**Save** não fecha o **Recordset** ou *Destination*, então você poderá continuar trabalhando com o **Recordset** e salvar suas alterações mais recentes. *Destination* permanecerá aberto até que o **Recordset** seja fechado e, durante esse tempo, outros aplicativos poderá ler mas não gravar em *Destination*.</span><span class="sxs-lookup"><span data-stu-id="52aac-p106">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed, during which time other applications can read but not write to *Destination*.</span></span>

<span data-ttu-id="52aac-p107">Por motivos de segurança, o método **Save** permite apenas a utilização de definições de segurança baixas e personalizadas a partir de um script executado pelo Microsoft Internet Explorer. Para obter uma explicação mais detalhada dos problemas de segurança, consulte "ADO and RDS Security Issues in Microsoft Internet Explorer" sob Artigos Técnicos do ActiveX Data Objects (ADO) nos Artigos Técnicos de Acesso a Dados da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="52aac-p107">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="52aac-129">Se o método **Save** for chamado enquanto uma operação de busca, execução ou atualização assíncrona de **Recordset** estiver em andamento, **Save** aguardará até que a operação assíncrona seja concluída.</span><span class="sxs-lookup"><span data-stu-id="52aac-129">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="52aac-p108">Os registros são salvos a partir da primeira linha do **Recordset**. Quando o método **Save** for concluído, a posição de linha atual será movida para a primeira linha do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="52aac-p108">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="52aac-p109">Para obter melhores resultados, defina a propriedade [CursorLocation](cursorlocation-property-ado.md) para **adUseClient** com **Save**. Se o provedor não oferecer suporte a toda a funcionalidade necessária para salvar objetos **Recordset**, o Cursor Service fornecerá essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="52aac-p109">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="52aac-p110">Quando um **Recordset** for mantido com a propriedade **CursorLocation** definida como **adUseServer**, a capacidade de atualização do **Recordset** será limitada. Normalmente, apenas atualizações, inserções e exclusões de tabela única são permitidas (dependendo da funcionalidade do provedor). O método [Resync](resync-method-ado.md) também está indisponível nessa configuração.</span><span class="sxs-lookup"><span data-stu-id="52aac-p110">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>

<span data-ttu-id="52aac-137">Porque o parâmetro *Destination* pode aceitar qualquer objeto que dá suporte à interface **IStream** do OLE DB, você pode salvar um **Recordset** diretamente para o objeto de **resposta** do ASP.</span><span class="sxs-lookup"><span data-stu-id="52aac-137">Because the *Destination* parameter can accept any object that supports the OLE DB **IStream** interface, you can save a **Recordset** directly to the ASP **Response** object.</span></span>

<span data-ttu-id="52aac-138">No exemplo a seguir, os métodos **Save** e **Open** são usados para manter um **Recordset** e reabri-lo posteriormente:</span><span class="sxs-lookup"><span data-stu-id="52aac-138">In the following example, the **Save** and **Open** methods are used to persist a **Recordset** and later reopen it:</span></span>

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

<span data-ttu-id="52aac-139">Esta seção inclui os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="52aac-139">This section includes the following topics:</span></span>

- [<span data-ttu-id="52aac-140">Mais informações sobre a persistência do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="52aac-140">More About Recordset Persistence</span></span>](more-about-recordset-persistence.md)

- [<span data-ttu-id="52aac-141">Conjuntos de registros persistentes filtrados e hierárquicos</span><span class="sxs-lookup"><span data-stu-id="52aac-141">Persisting Filtered and Hierarchical Recordsets</span></span>](persisting-filtered-and-hierarchical-recordsets.md)

- [<span data-ttu-id="52aac-142">Mantendo registros em formato XML (ADO)</span><span class="sxs-lookup"><span data-stu-id="52aac-142">Persisting Records in XML Format (ADO)</span></span>](persisting-records-in-xml-format.md)