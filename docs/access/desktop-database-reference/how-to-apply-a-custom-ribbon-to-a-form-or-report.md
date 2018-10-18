---
<span data-ttu-id="44cd3-101">título: aplicar uma faixa de opções personalizada a um formulário ou relatório TOCTitle: aplicar uma faixa de opções personalizada a um formulário ou relatório <<<<<<< ms:assetid cabeça: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: ms.date 48545865: 18/09/2015 === === Descrição: como aplicar faixas de opções personalizadas ao carregar um formulário ou relatório no Access 2013.</span><span class="sxs-lookup"><span data-stu-id="44cd3-101">title: Apply a custom ribbon to a form or report TOCTitle: Apply a custom ribbon to a form or report <<<<<<< HEAD ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 09/18/2015 ======= description: How to apply customized ribbons when loading a form or report in Access 2013.</span></span>
<span data-ttu-id="44cd3-102">MS:AssetID: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: ms.date 48545865: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="44cd3-102">ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="44cd3-103">mtps_version mestre: v=office.15</span><span class="sxs-lookup"><span data-stu-id="44cd3-103">master mtps_version: v=office.15</span></span>
---

# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="44cd3-104">Aplicar uma faixa de opções personalizada a um formulário ou relatório</span><span class="sxs-lookup"><span data-stu-id="44cd3-104">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="44cd3-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="44cd3-105"><<<<<<< HEAD</span></span>

<span data-ttu-id="44cd3-106">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="44cd3-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="44cd3-107">A faixa de opções usa marcação XML declarativa baseada em texto que simplifica a criação e a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="44cd3-107">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="44cd3-108">Com algumas linhas de XML, você pode criar a interface exata para o usuário.</span><span class="sxs-lookup"><span data-stu-id="44cd3-108">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="44cd3-109">Access oferece flexibilidade na personalização da interface do usuário da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="44cd3-109">Access provides flexibility in customizing the ribbon user interface.</span></span> <span data-ttu-id="44cd3-110">Por exemplo, a marcação de personalização pode ser armazenada em uma tabela, inserida em um procedimento VBA, armazenado em outro banco de dados do Access, ou vinculado a ele, de uma planilha do Excel.</span><span class="sxs-lookup"><span data-stu-id="44cd3-110">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="44cd3-111">Este tópico descreve como aplicar faixas de opções personalizadas ao carregar um formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="44cd3-111">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="44cd3-112">Disponibilizando o XML de personalização da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="44cd3-112">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="44cd3-113">**Armazenando o XML de Extensibilidade da Faixa de Opções em uma tabela**</span><span class="sxs-lookup"><span data-stu-id="44cd3-113">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="44cd3-p103">Um método que você pode usar para disponibilizar personalizações da faixa de opção é armazená-las em uma tabela chamada **USysRibbons**, as personalizações poderão ser implementadas sem o uso de macros ou de código VBA.</span><span class="sxs-lookup"><span data-stu-id="44cd3-p103">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="44cd3-p104">**USysRibbons** é uma tabela do sistema criada pelo usuário. A tabela deve ser criada usando nomes de coluna específicas para que as personalizações da faixa de opções sejam implementadas. A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="44cd3-p104">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
=======
<span data-ttu-id="44cd3-119">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="44cd3-119">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="44cd3-120">A faixa de opções usa marcação XML declarativa baseada em texto que simplifica a criação e a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="44cd3-120">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="44cd3-121">Com algumas linhas de XML, você pode criar a interface exata para o usuário.</span><span class="sxs-lookup"><span data-stu-id="44cd3-121">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="44cd3-122">Access oferece flexibilidade na personalização da interface do usuário da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="44cd3-122">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="44cd3-123">Por exemplo, a marcação de personalização pode ser armazenada em uma tabela, inserida em um procedimento VBA, armazenado em outro banco de dados do Access, ou vinculado a ele, de uma planilha do Excel.</span><span class="sxs-lookup"><span data-stu-id="44cd3-123">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="44cd3-124">Este tópico descreve como aplicar faixas de opções personalizadas ao carregar um formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="44cd3-124">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="44cd3-125">Disponibilizar o XML de personalização da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="44cd3-125">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="44cd3-126">Extensibilidade da faixa de opções do repositório XML em uma tabela</span><span class="sxs-lookup"><span data-stu-id="44cd3-126">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="44cd3-p107">Um método que você pode usar para disponibilizar personalizações da faixa de opção é armazená-las em uma tabela chamada **USysRibbons**, as personalizações poderão ser implementadas sem o uso de macros ou de código VBA.</span><span class="sxs-lookup"><span data-stu-id="44cd3-p107">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="44cd3-129">**USysRibbons** é uma tabela do sistema criada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="44cd3-129">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="44cd3-130">A tabela deve ser criada com o uso de nomes de coluna específica para as personalizações de faixa de opções a serem implementadas.</span><span class="sxs-lookup"><span data-stu-id="44cd3-130">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="44cd3-131">A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="44cd3-131">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="44cd3-132">mestre</span><span class="sxs-lookup"><span data-stu-id="44cd3-132">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="44cd3-133"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="44cd3-133"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="44cd3-134">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="44cd3-134">Column Name</span></span></p></th>
<th><p><span data-ttu-id="44cd3-135">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="44cd3-135">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="44cd3-136">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="44cd3-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="44cd3-137">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="44cd3-137">Data type</span></span></p></th><span data-ttu-id="44cd3-138">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="44cd3-138">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="44cd3-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="44cd3-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44cd3-140"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="44cd3-140"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="44cd3-141">Texto</span><span class="sxs-lookup"><span data-stu-id="44cd3-141">Text</span></span></p></td>
<span data-ttu-id="44cd3-142"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="44cd3-142"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="44cd3-143">Contém o nome da faixa de opções personalizada a ser associado essa personalização</span><span class="sxs-lookup"><span data-stu-id="44cd3-143">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
=======
<td><p><span data-ttu-id="44cd3-144">Contém o nome da faixa de opções personalizada a ser associado à esta personalização.</span><span class="sxs-lookup"><span data-stu-id="44cd3-144">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td><span data-ttu-id="44cd3-145">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="44cd3-145">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44cd3-146"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="44cd3-146"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="44cd3-147">Memorando</span><span class="sxs-lookup"><span data-stu-id="44cd3-147">Memo</span></span></p></td>
<span data-ttu-id="44cd3-148"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="44cd3-148"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="44cd3-149">Contém a faixa de opções Extensibility XML (RibbonX) que define a personalização da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="44cd3-149">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
=======
<td><p><span data-ttu-id="44cd3-150">Contém a extensibilidade da faixa de opções XML (RibbonX) que define a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="44cd3-150">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="44cd3-151">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="44cd3-151">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="44cd3-152"><<<<<<< Cabeça **Carregando extensibilidade da faixa de opções XML programaticamente**</span><span class="sxs-lookup"><span data-stu-id="44cd3-152"><<<<<<< HEAD **Loading Ribbon Extensibility XML Programmatically**</span></span>

<span data-ttu-id="44cd3-p109">Você pode usar o método **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** para carregar personalizações da faixa de opções programaticamente. Tipicamente, para criar e disponibilizar a faixa de opções para o aplicativo, primeiro você cria um módulo no banco de dados com um procedimento que chama o método **LoadCustomUI**, passando o nome da faixa de opções e a marcação de personalização do XML.</span><span class="sxs-lookup"><span data-stu-id="44cd3-p109">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="44cd3-155">Carregar a extensibilidade da faixa de opções XML programaticamente</span><span class="sxs-lookup"><span data-stu-id="44cd3-155">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="44cd3-p110">Você pode usar o método **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** para carregar personalizações da faixa de opções programaticamente. Tipicamente, para criar e disponibilizar a faixa de opções para o aplicativo, primeiro você cria um módulo no banco de dados com um procedimento que chama o método **LoadCustomUI**, passando o nome da faixa de opções e a marcação de personalização do XML.</span><span class="sxs-lookup"><span data-stu-id="44cd3-p110">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
>>>>>>> <span data-ttu-id="44cd3-158">mestre</span><span class="sxs-lookup"><span data-stu-id="44cd3-158">master</span></span>

<span data-ttu-id="44cd3-p111">A marcação XML pode vir de um objeto **Recordset** criado de uma tabela, de uma origem externa ao banco de dados como um arquivo XML analisado em uma cadeia de caracteres ou de uma marcação XML inserida diretamente no procedimento. Você pode criar faixas de opções diferentes usando várias chamadas ao método **LoadCustomUI**, passando marcação XML diferente desde que o nome de cada faixa de opções e o atributo **id** das guias que compõem a faixa de opções sejam exclusivas.</span><span class="sxs-lookup"><span data-stu-id="44cd3-p111">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="44cd3-p112">Após a conclusão do procedimento, você cria então uma macro AutoExec que chama o procedimento usando a ação RunCode. Dessa forma, quando o aplicativo for iniciado, o método **LoadCustomUI** será automaticamente executado e todas as faixas de opções personalizadas serão disponibilizadas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44cd3-p112">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

<span data-ttu-id="44cd3-163"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="44cd3-163"><<<<<<< HEAD</span></span>
## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="44cd3-164">Atribuindo faixas de opções personalizadas a formulários ou relatórios</span><span class="sxs-lookup"><span data-stu-id="44cd3-164">Assigning Custom Ribbons to Forms or Reports</span></span>
=======
## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="44cd3-165">Atribuir faixas de opções personalizadas para formulários ou relatórios</span><span class="sxs-lookup"><span data-stu-id="44cd3-165">Assign custom ribbons to forms or reports</span></span>
>>>>>>> <span data-ttu-id="44cd3-166">mestre</span><span class="sxs-lookup"><span data-stu-id="44cd3-166">master</span></span>

1.  <span data-ttu-id="44cd3-167">Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44cd3-167">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="44cd3-168">Abra o formulário ou relatório no modo de Design.</span><span class="sxs-lookup"><span data-stu-id="44cd3-168">Open the form or report in Design view.</span></span>

<span data-ttu-id="44cd3-169"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="44cd3-169"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="44cd3-170">Na guia Design, clique em **Folha de propriedades**.</span><span class="sxs-lookup"><span data-stu-id="44cd3-170">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="44cd3-171">Na guia **Todas** da janela Propriedade, clique na lista **Nome da Faixa de Opções** e selecione uma Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="44cd3-171">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>
=======
3.  <span data-ttu-id="44cd3-172">Na guia Design, escolha a **Folha de propriedades**.</span><span class="sxs-lookup"><span data-stu-id="44cd3-172">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="44cd3-173">Na guia **todas** da janela propriedade, escolha a lista **Nome da faixa de opções** e selecione uma faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="44cd3-173">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>
>>>>>>> <span data-ttu-id="44cd3-174">mestre</span><span class="sxs-lookup"><span data-stu-id="44cd3-174">master</span></span>

5.  <span data-ttu-id="44cd3-175">Salve, feche e reabra o formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="44cd3-175">Save, close, and then reopen the form or report.</span></span> <span data-ttu-id="44cd3-176">A faixa de opções da interface do usuário selecionado é exibida.</span><span class="sxs-lookup"><span data-stu-id="44cd3-176">The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="44cd3-177">As guias exibidas na interface do usuário da faixa de opções são aditivas.</span><span class="sxs-lookup"><span data-stu-id="44cd3-177">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="44cd3-178">Ou seja, a menos que especificamente ocultar as guias ou definir o atributo *começar do zero* como **True**, as guias exibidas em um formulário ou interface de usuário da faixa de opções do relatório estão além das guias existentes.</span><span class="sxs-lookup"><span data-stu-id="44cd3-178">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="44cd3-179">[!OBSERVAçãO] Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="44cd3-179">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


