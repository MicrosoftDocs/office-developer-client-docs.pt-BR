---
title: Aplicar uma faixa de opções personalizada a um formulário ou relatório
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464552"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="ca8e5-102">Aplicar uma faixa de opções personalizada a um formulário ou relatório</span><span class="sxs-lookup"><span data-stu-id="ca8e5-102">Apply a custom ribbon to a form or report</span></span>


<span data-ttu-id="ca8e5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca8e5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ca8e5-104">A faixa de opções usa marcação XML declarativa baseada em texto que simplifica a criação e a personalização da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-104">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="ca8e5-105">Com algumas linhas de XML, você pode criar a interface exata para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-105">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="ca8e5-106">Access oferece flexibilidade na personalização da interface do usuário da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-106">Access provides flexibility in customizing the ribbon user interface.</span></span> <span data-ttu-id="ca8e5-107">Por exemplo, a marcação de personalização pode ser armazenada em uma tabela, inserida em um procedimento VBA, armazenado em outro banco de dados do Access, ou vinculado a ele, de uma planilha do Excel.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-107">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="ca8e5-108">Este tópico descreve como aplicar faixas de opções personalizadas ao carregar um formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-108">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="ca8e5-109">Disponibilizando o XML de personalização da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="ca8e5-109">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="ca8e5-110">**Armazenando o XML de Extensibilidade da Faixa de Opções em uma tabela**</span><span class="sxs-lookup"><span data-stu-id="ca8e5-110">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="ca8e5-p102">Um método que você pode usar para disponibilizar personalizações da faixa de opção é armazená-las em uma tabela chamada **USysRibbons**, as personalizações poderão ser implementadas sem o uso de macros ou de código VBA.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-p102">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="ca8e5-p103">**USysRibbons** é uma tabela do sistema criada pelo usuário. A tabela deve ser criada usando nomes de coluna específicas para que as personalizações da faixa de opções sejam implementadas. A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-p103">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca8e5-116">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="ca8e5-116">Column Name</span></span></p></th>
<th><p><span data-ttu-id="ca8e5-117">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ca8e5-117">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ca8e5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca8e5-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca8e5-119"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="ca8e5-119"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="ca8e5-120">Texto</span><span class="sxs-lookup"><span data-stu-id="ca8e5-120">Text</span></span></p></td>
<td><p><span data-ttu-id="ca8e5-121">Contém o nome da faixa de opções personalizada a ser associado essa personalização</span><span class="sxs-lookup"><span data-stu-id="ca8e5-121">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca8e5-122"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="ca8e5-122"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="ca8e5-123">Memorando</span><span class="sxs-lookup"><span data-stu-id="ca8e5-123">Memo</span></span></p></td>
<td><p><span data-ttu-id="ca8e5-124">Contém a faixa de opções Extensibility XML (RibbonX) que define a personalização da faixa de opções</span><span class="sxs-lookup"><span data-stu-id="ca8e5-124">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ca8e5-125">**Carregando o XML de Extensibilidade da Faixa de Opções programaticamente**</span><span class="sxs-lookup"><span data-stu-id="ca8e5-125">**Loading Ribbon Extensibility XML Programmatically**</span></span>

<span data-ttu-id="ca8e5-p104">Você pode usar o método **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** para carregar personalizações da faixa de opções programaticamente. Tipicamente, para criar e disponibilizar a faixa de opções para o aplicativo, primeiro você cria um módulo no banco de dados com um procedimento que chama o método **LoadCustomUI**, passando o nome da faixa de opções e a marcação de personalização do XML.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-p104">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="ca8e5-p105">A marcação XML pode vir de um objeto **Recordset** criado de uma tabela, de uma origem externa ao banco de dados como um arquivo XML analisado em uma cadeia de caracteres ou de uma marcação XML inserida diretamente no procedimento. Você pode criar faixas de opções diferentes usando várias chamadas ao método **LoadCustomUI**, passando marcação XML diferente desde que o nome de cada faixa de opções e o atributo **id** das guias que compõem a faixa de opções sejam exclusivas.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-p105">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="ca8e5-p106">Após a conclusão do procedimento, você cria então uma macro AutoExec que chama o procedimento usando a ação RunCode. Dessa forma, quando o aplicativo for iniciado, o método **LoadCustomUI** será automaticamente executado e todas as faixas de opções personalizadas serão disponibilizadas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-p106">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="ca8e5-132">Atribuindo faixas de opções personalizadas a formulários ou relatórios</span><span class="sxs-lookup"><span data-stu-id="ca8e5-132">Assigning Custom Ribbons to Forms or Reports</span></span>

1.  <span data-ttu-id="ca8e5-133">Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-133">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="ca8e5-134">Abra o formulário ou relatório no modo de Design.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-134">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="ca8e5-135">Na guia Design, clique em **Folha de propriedades**.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-135">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="ca8e5-136">Na guia **Todas** da janela Propriedade, clique na lista **Nome da Faixa de Opções** e selecione uma Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-136">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="ca8e5-137">Salve, feche e reabra o formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-137">Save, close, and then reopen the form or report.</span></span> <span data-ttu-id="ca8e5-138">A faixa de opções da interface do usuário selecionado é exibida.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-138">The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="ca8e5-139">As guias exibidas na interface do usuário da faixa de opções são aditivas.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-139">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="ca8e5-140">Ou seja, a menos que especificamente ocultar as guias ou definir o atributo *começar do zero* como **True**, as guias exibidas em um formulário ou interface de usuário da faixa de opções do relatório estão além das guias existentes.</span><span class="sxs-lookup"><span data-stu-id="ca8e5-140">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="ca8e5-141">[!OBSERVAçãO] Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="ca8e5-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


