---
title: Aplicar uma faixa de opções personalizada ao iniciar o Access
TOCTitle: Apply a custom ribbon when starting Access
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 575834f818386a7ba536e826fff2b7da00b324d5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465475"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="5a715-102">Aplicar uma faixa de opções personalizada ao iniciar o Access</span><span class="sxs-lookup"><span data-stu-id="5a715-102">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="5a715-103">**Aplica-se a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a715-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="5a715-p101">A faixa de opções usa marcação XML declarativa baseada em texto que simplifica a criação e a personalização da faixa de opções. Com algumas linhas de XML, você pode criar a interface exata para o usuário. O Access oferece uma flexibilidade extraordinária na personalização da interface do usuário da faixa de opções. Por exemplo, a marcação de personalização pode ser armazenada em uma tabela, inserida em um procedimento VBA, armazenado em outro banco de dados do Access, ou vinculado a ele, de uma planilha do Excel. Este tópico descreve como aplicar faixas de opção personalizadas ao abrir um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5a715-p101">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides tremendous flexibility in customizing the ribbon UI. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when opening a database.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="5a715-109">Disponibilizando o XML de personalização da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="5a715-109">Making the Ribbon Customization XML Available</span></span>

### <a name="storing-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="5a715-110">Armazenando o XML de Extensibilidade da Faixa de Opções em uma tabela</span><span class="sxs-lookup"><span data-stu-id="5a715-110">Storing Ribbon Extensibility XML in a Table</span></span>

<span data-ttu-id="5a715-p102">Um método que você pode usar para disponibilizar personalizações da faixa de opção é armazená-las em uma tabela chamada **USysRibbons**, as personalizações poderão ser implementadas sem o uso de macros ou de código VBA.</span><span class="sxs-lookup"><span data-stu-id="5a715-p102">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="5a715-p103">**USysRibbons** é uma tabela do sistema criada pelo usuário. A tabela deve ser criada usando nomes de coluna específicas para que as personalizações da faixa de opções sejam implementadas. A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="5a715-p103">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a715-116">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="5a715-116">Column Name</span></span></p></th>
<th><p><span data-ttu-id="5a715-117">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5a715-117">Data Type</span></span></p></th>
<th><p><span data-ttu-id="5a715-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a715-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a715-119"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="5a715-119"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="5a715-120">Texto</span><span class="sxs-lookup"><span data-stu-id="5a715-120">Text</span></span></p></td>
<td><p><span data-ttu-id="5a715-121">Contém o nome da faixa de opções personalizada a ser associado à esta personalização.</span><span class="sxs-lookup"><span data-stu-id="5a715-121">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a715-122"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="5a715-122"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="5a715-123">Memorando</span><span class="sxs-lookup"><span data-stu-id="5a715-123">Memo</span></span></p></td>
<td><p><span data-ttu-id="5a715-124">Contém o XML de Extensibilidade da Faixa de Opções (RibbonX) que define a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="5a715-124">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="loading-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="5a715-125">Carregando o XML de Extensibilidade da Faixa de Opções programaticamente</span><span class="sxs-lookup"><span data-stu-id="5a715-125">Loading Ribbon Extensibility XML Programmatically</span></span>

<span data-ttu-id="5a715-p104">Você pode usar o método **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** para carregar personalizações da faixa de opções programaticamente. Tipicamente, para criar e disponibilizar a faixa de opções para o aplicativo, primeiro você cria um módulo no banco de dados com um procedimento que chama o método **LoadCustomUI**, passando o nome da faixa de opções e a marcação de personalização do XML.</span><span class="sxs-lookup"><span data-stu-id="5a715-p104">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="5a715-p105">A marcação XML pode vir de um objeto **Recordset** criado de uma tabela, de uma origem externa ao banco de dados como um arquivo XML analisado em uma cadeia de caracteres ou de uma marcação XML inserida diretamente no procedimento. Você pode criar faixas de opções diferentes usando várias chamadas ao método **LoadCustomUI**, passando marcação XML diferente desde que o nome de cada faixa de opções e o atributo **id** das guias que compõem a faixa de opções sejam exclusivas.</span><span class="sxs-lookup"><span data-stu-id="5a715-p105">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="5a715-p106">Após a conclusão do procedimento, você cria então uma macro AutoExec que chama o procedimento usando a ação RunCode. Dessa forma, quando o aplicativo for iniciado, o método **LoadCustomUI** será automaticamente executado e todas as faixas de opções personalizadas serão disponibilizadas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5a715-p106">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="applying-customized-ribbons-when-access-starts"></a><span data-ttu-id="5a715-132">Aplicando faixas de opções personalizadas quando o Access é iniciado</span><span class="sxs-lookup"><span data-stu-id="5a715-132">Applying Customized Ribbons When Access Starts</span></span>

<span data-ttu-id="5a715-133">Para aplicar uma interface do usuário personalizada de forma que ela esteja disponível quando o aplicativo for iniciado, use este procedimento:</span><span class="sxs-lookup"><span data-stu-id="5a715-133">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="5a715-134">Siga o processo descrito anteriormente para disponibilizar as faixas de opções personalizadas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5a715-134">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="5a715-135">Feche e então reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5a715-135">Close and then restart the application.</span></span>

3.  <span data-ttu-id="5a715-136">Clique no **Botão do Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") e clique em **Opções do Access**.</span><span class="sxs-lookup"><span data-stu-id="5a715-136">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="5a715-137">Clique na opção **Banco de Dados Atual** e então, na seção **Opções da Faixa de Opções e da Barra de Ferramentas**, clique na lista **Nome da Faixa de Opções** e selecione uma faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="5a715-137">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select a ribbon.</span></span>

5.  <span data-ttu-id="5a715-p107">Agora feche e reinicie o aplicativo. A interface do usuário selecionada será exibida.</span><span class="sxs-lookup"><span data-stu-id="5a715-p107">Now close and restart the application. The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="5a715-140">[!OBSERVAçãO] Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="5a715-140">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


