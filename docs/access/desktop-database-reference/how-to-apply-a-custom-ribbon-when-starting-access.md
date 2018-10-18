---
<span data-ttu-id="21232-101">título: aplicar uma faixa de opções personalizada ao iniciar o Access TOCTitle: aplicar uma faixa de opções personalizada ao iniciar o Access <<<<<<< ms:assetid cabeça: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: ms.date 48546659: 09/18 / 2015 === Descrição: como aplicar faixas de opções personalizadas ao abrir um banco de dados do Access 2013.</span><span class="sxs-lookup"><span data-stu-id="21232-101">title: Apply a custom ribbon when starting Access TOCTitle: Apply a custom ribbon when starting Access <<<<<<< HEAD ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: 48546659 ms.date: 09/18/2015 ======= description: How to apply customized ribbons when opening a database in Access 2013.</span></span> <span data-ttu-id="21232-102">MS:AssetID: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: ms.date 48546659: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="21232-102">ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: 48546659 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="21232-103">mtps_version mestre: v=office.15</span><span class="sxs-lookup"><span data-stu-id="21232-103">master mtps_version: v=office.15</span></span>
---

# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="21232-104">Aplicar uma faixa de opções personalizada ao iniciar o Access</span><span class="sxs-lookup"><span data-stu-id="21232-104">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="21232-105">**Aplica-se a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="21232-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="21232-p102">A faixa de opções usa marcação XML declarativa baseada em texto que simplifica a criação e a personalização da faixa de opções. Com algumas linhas de XML, você pode criar a interface exata para o usuário. O Access oferece uma flexibilidade extraordinária na personalização da interface do usuário da faixa de opções. Por exemplo, a marcação de personalização pode ser armazenada em uma tabela, inserida em um procedimento VBA, armazenado em outro banco de dados do Access, ou vinculado a ele, de uma planilha do Excel. Este tópico descreve como aplicar faixas de opção personalizadas ao abrir um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="21232-p102">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides tremendous flexibility in customizing the ribbon UI. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when opening a database.</span></span>

<span data-ttu-id="21232-111"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="21232-111"><<<<<<< HEAD</span></span>
## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="21232-112">Disponibilizando o XML de personalização da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="21232-112">Making the Ribbon Customization XML Available</span></span>

### <a name="storing-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="21232-113">Armazenando o XML de Extensibilidade da Faixa de Opções em uma tabela</span><span class="sxs-lookup"><span data-stu-id="21232-113">Storing Ribbon Extensibility XML in a Table</span></span>

<span data-ttu-id="21232-p103">Um método que você pode usar para disponibilizar personalizações da faixa de opção é armazená-las em uma tabela chamada **USysRibbons**, as personalizações poderão ser implementadas sem o uso de macros ou de código VBA.</span><span class="sxs-lookup"><span data-stu-id="21232-p103">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="21232-p104">**USysRibbons** é uma tabela do sistema criada pelo usuário. A tabela deve ser criada usando nomes de coluna específicas para que as personalizações da faixa de opções sejam implementadas. A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="21232-p104">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
=======
## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="21232-119">Disponibilizar o XML de personalização da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="21232-119">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="21232-120">Extensibilidade da faixa de opções do repositório XML em uma tabela</span><span class="sxs-lookup"><span data-stu-id="21232-120">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="21232-p105">Um método que você pode usar para disponibilizar personalizações da faixa de opção é armazená-las em uma tabela chamada **USysRibbons**, as personalizações poderão ser implementadas sem o uso de macros ou de código VBA.</span><span class="sxs-lookup"><span data-stu-id="21232-p105">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="21232-123">**USysRibbons** é uma tabela do sistema criada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="21232-123">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="21232-124">A tabela deve ser criada com o uso de nomes de coluna específica para as personalizações de faixa de opções a serem implementadas.</span><span class="sxs-lookup"><span data-stu-id="21232-124">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="21232-125">A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="21232-125">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="21232-126">mestre</span><span class="sxs-lookup"><span data-stu-id="21232-126">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="21232-127"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="21232-127"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="21232-128">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="21232-128">Column Name</span></span></p></th>
<th><p><span data-ttu-id="21232-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="21232-129">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="21232-130">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="21232-130">Column name</span></span></p></th>
<th><p><span data-ttu-id="21232-131">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="21232-131">Data type</span></span></p></th><span data-ttu-id="21232-132">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="21232-132">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="21232-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="21232-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21232-134"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="21232-134"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="21232-135">Texto</span><span class="sxs-lookup"><span data-stu-id="21232-135">Text</span></span></p></td>
<td><p><span data-ttu-id="21232-136">Contém o nome da faixa de opções personalizada a ser associado à esta personalização.</span><span class="sxs-lookup"><span data-stu-id="21232-136">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21232-137"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="21232-137"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="21232-138">Memorando</span><span class="sxs-lookup"><span data-stu-id="21232-138">Memo</span></span></p></td>
<span data-ttu-id="21232-139"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="21232-139"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="21232-140">Contém o XML de Extensibilidade da Faixa de Opções (RibbonX) que define a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="21232-140">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
=======
<td><p><span data-ttu-id="21232-141">Contém a extensibilidade da faixa de opções XML (RibbonX) que define a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="21232-141">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="21232-142">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="21232-142">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="21232-143"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="21232-143"><<<<<<< HEAD</span></span>
### <a name="loading-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="21232-144">Carregando o XML de Extensibilidade da Faixa de Opções programaticamente</span><span class="sxs-lookup"><span data-stu-id="21232-144">Loading Ribbon Extensibility XML Programmatically</span></span>

<span data-ttu-id="21232-p107">Você pode usar o método **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** para carregar personalizações da faixa de opções programaticamente. Tipicamente, para criar e disponibilizar a faixa de opções para o aplicativo, primeiro você cria um módulo no banco de dados com um procedimento que chama o método **LoadCustomUI**, passando o nome da faixa de opções e a marcação de personalização do XML.</span><span class="sxs-lookup"><span data-stu-id="21232-p107">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="21232-p108">A marcação XML pode vir de um objeto **Recordset** criado de uma tabela, de uma origem externa ao banco de dados como um arquivo XML analisado em uma cadeia de caracteres ou de uma marcação XML inserida diretamente no procedimento. Você pode criar faixas de opções diferentes usando várias chamadas ao método **LoadCustomUI**, passando marcação XML diferente desde que o nome de cada faixa de opções e o atributo **id** das guias que compõem a faixa de opções sejam exclusivas.</span><span class="sxs-lookup"><span data-stu-id="21232-p108">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="21232-p109">Após a conclusão do procedimento, você cria então uma macro AutoExec que chama o procedimento usando a ação RunCode. Dessa forma, quando o aplicativo for iniciado, o método **LoadCustomUI** será automaticamente executado e todas as faixas de opções personalizadas serão disponibilizadas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21232-p109">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="applying-customized-ribbons-when-access-starts"></a><span data-ttu-id="21232-151">Aplicando faixas de opções personalizadas quando o Access é iniciado</span><span class="sxs-lookup"><span data-stu-id="21232-151">Applying Customized Ribbons When Access Starts</span></span>
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="21232-152">Carregar a extensibilidade da faixa de opções XML programaticamente</span><span class="sxs-lookup"><span data-stu-id="21232-152">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="21232-p110">Você pode usar o método **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** para carregar personalizações da faixa de opções programaticamente. Tipicamente, para criar e disponibilizar a faixa de opções para o aplicativo, primeiro você cria um módulo no banco de dados com um procedimento que chama o método **LoadCustomUI**, passando o nome da faixa de opções e a marcação de personalização do XML.</span><span class="sxs-lookup"><span data-stu-id="21232-p110">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="21232-p111">A marcação XML pode vir de um objeto **Recordset** criado de uma tabela, de uma origem externa ao banco de dados como um arquivo XML analisado em uma cadeia de caracteres ou de uma marcação XML inserida diretamente no procedimento. Você pode criar faixas de opções diferentes usando várias chamadas ao método **LoadCustomUI**, passando marcação XML diferente desde que o nome de cada faixa de opções e o atributo **id** das guias que compõem a faixa de opções sejam exclusivas.</span><span class="sxs-lookup"><span data-stu-id="21232-p111">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="21232-157">Após a conclusão do procedimento, você cria então uma macro AutoExec que chama o procedimento usando a ação RunCode.</span><span class="sxs-lookup"><span data-stu-id="21232-157">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="21232-158">Dessa forma, quando o aplicativo for iniciado, o método **LoadCustomUI** será executado automaticamente e todas as faixas de opções personalizadas são disponibilizadas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21232-158">That way, when the application is started, the **LoadCustomUI** method is automatically executed, and all of the custom ribbons are made available to the application.</span></span>

## <a name="apply-customized-ribbons-when-access-starts"></a><span data-ttu-id="21232-159">Aplicar faixas de opções personalizadas ao iniciar o Access</span><span class="sxs-lookup"><span data-stu-id="21232-159">Apply customized ribbons when Access starts</span></span>
>>>>>>> <span data-ttu-id="21232-160">mestre</span><span class="sxs-lookup"><span data-stu-id="21232-160">master</span></span>

<span data-ttu-id="21232-161">Para aplicar uma interface do usuário personalizada de forma que ela esteja disponível quando o aplicativo for iniciado, use este procedimento:</span><span class="sxs-lookup"><span data-stu-id="21232-161">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="21232-162">Siga o processo descrito anteriormente para disponibilizar as faixas de opções personalizadas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21232-162">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="21232-163">Feche e então reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21232-163">Close and then restart the application.</span></span>

<span data-ttu-id="21232-164"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="21232-164"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="21232-165">Clique no **Botão do Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") e clique em **Opções do Access**.</span><span class="sxs-lookup"><span data-stu-id="21232-165">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="21232-166">Clique na opção **Banco de Dados Atual** e então, na seção **Opções da Faixa de Opções e da Barra de Ferramentas**, clique na lista **Nome da Faixa de Opções** e selecione uma faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="21232-166">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select a ribbon.</span></span>
=======
3.  <span data-ttu-id="21232-167">Escolha o **Botão do Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") e escolha **Opções do Access**.</span><span class="sxs-lookup"><span data-stu-id="21232-167">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="21232-168">Escolha a opção de **Banco de dados atual** e em seguida, na seção **Opções de barra de ferramentas e faixa de opções** , escolha a lista **Nome da faixa de opções** e selecione uma faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="21232-168">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select a ribbon.</span></span>
>>>>>>> <span data-ttu-id="21232-169">mestre</span><span class="sxs-lookup"><span data-stu-id="21232-169">master</span></span>

5.  <span data-ttu-id="21232-p113">Agora feche e reinicie o aplicativo. A interface do usuário selecionada será exibida.</span><span class="sxs-lookup"><span data-stu-id="21232-p113">Now close and restart the application. The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="21232-172">[!OBSERVAçãO] Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="21232-172">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


