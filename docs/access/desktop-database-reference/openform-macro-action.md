---
title: Ação da macro AbrirFormulário
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf89b61a65c11f09d5a07e52caeee5ad416c118a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288368"
---
# <a name="openform-macro-action"></a><span data-ttu-id="cc876-102">Ação da macro AbrirFormulário</span><span class="sxs-lookup"><span data-stu-id="cc876-102">OpenForm macro action</span></span>

<span data-ttu-id="cc876-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc876-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc876-104">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view.</span><span class="sxs-lookup"><span data-stu-id="cc876-104">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view.</span></span> <span data-ttu-id="cc876-105">Você pode selecionar a entrada de dados e os modos de janela para o formulário e restringir os registros que o formulário exibe.</span><span class="sxs-lookup"><span data-stu-id="cc876-105">You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="cc876-106">Setting</span><span class="sxs-lookup"><span data-stu-id="cc876-106">Setting</span></span>

<span data-ttu-id="cc876-107">A **ação OpenForm** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="cc876-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc876-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="cc876-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cc876-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc876-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc876-110"><strong>Nome do formulário</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-111">O nome do formulário a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="cc876-111">The name of the form to open.</span></span> <span data-ttu-id="cc876-112">A <strong>caixa Nome do</strong> Formulário na seção <strong>Argumentos da</strong> Ação do painel Construtor de Macros mostra todos os formulários no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="cc876-112">The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database.</span></span> <span data-ttu-id="cc876-113">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cc876-113">This is a required argument.</span></span> <span data-ttu-id="cc876-114">Se você executar uma macro contendo a ação <strong>OpenForm</strong> em um banco de dados biblioteca, o Microsoft Access primeiro procura o formulário com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="cc876-114">If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc876-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-116">O exibição no qual o formulário será aberto.</span><span class="sxs-lookup"><span data-stu-id="cc876-116">The view in which the form will open.</span></span> <span data-ttu-id="cc876-117">Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span><span class="sxs-lookup"><span data-stu-id="cc876-117">Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="cc876-118">O padrão é <strong>Form</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc876-118">The default is <strong>Form</strong>.</span></span></p><p><span data-ttu-id="cc876-119"><strong>OBSERVAÇÃO:</strong>a <STRONG>configuração</STRONG> do argumento View substitui as configurações das propriedades <STRONG>DefaultView</STRONG> e <STRONG>ViewsAllowed do</STRONG> formulário.</span><span class="sxs-lookup"><span data-stu-id="cc876-119"><strong>NOTE</strong>: The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties.</span></span> <span data-ttu-id="cc876-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span><span class="sxs-lookup"><span data-stu-id="cc876-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc876-121"><strong>Nome do Filtro</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-122">Um filtro que restringe ou classifica os registros do formulário.</span><span class="sxs-lookup"><span data-stu-id="cc876-122">A filter that restricts or sorts the form's records.</span></span> <span data-ttu-id="cc876-123">Você pode digitar o nome de uma consulta existente ou de um filtro que foi salvo como consulta.</span><span class="sxs-lookup"><span data-stu-id="cc876-123">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="cc876-124">No entanto, a consulta deve incluir todos os campos no formulário que você está abrindo ou ter sua <strong>propriedade OutputAllFields</strong> definida como <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc876-124">However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc876-125"><strong>Condição Where</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-126">Uma cláusula SQL WHERE válida (sem a palavra WHERE) ou expressão que o Access usa para selecionar registros da tabela ou consulta base do formulário.</span><span class="sxs-lookup"><span data-stu-id="cc876-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="cc876-127">Se você selecionar um filtro com o argumento <strong>Nome do Filtro</strong>, o Access aplicará essa cláusula WHERE aos resultados do filtro.</span><span class="sxs-lookup"><span data-stu-id="cc876-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="cc876-128">Para abrir um formulário e restringir seus registros àqueles especificados pelo valor de um controle em outro formulário, use a expressão a seguir: <strong>[</strong><em>nome_do_campo</em><strong>] = Formulários![</strong> <em>formname</em><strong>]! [</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span><span class="sxs-lookup"><span data-stu-id="cc876-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="cc876-129">Substitua <em>formname</em> e <em>controlname em outro</em> formulário pelo nome do outro formulário e o controle no outro formulário que contém o valor que você deseja que os registros do primeiro formulário sejam match.</span><span class="sxs-lookup"><span data-stu-id="cc876-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p><p><span data-ttu-id="cc876-130"><strong>OBSERVAÇÃO:</strong>o comprimento máximo do argumento <STRONG>Condição Where</STRONG> é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cc876-130"><strong>NOTE</strong>: The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters.</span></span> <span data-ttu-id="cc876-131">Se você precisar inserir uma cláusula SQL WHERE mais complexa do que essa, use o método <STRONG>OpenForm</STRONG> do objeto <STRONG>DoCmd</STRONG> em um módulo do VBA (Visual Basic for Applications).</span><span class="sxs-lookup"><span data-stu-id="cc876-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="cc876-132">É possível inserir instruções de cláusulas SQL WHERE de até 32.768 caracteres no VBA.</span><span class="sxs-lookup"><span data-stu-id="cc876-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc876-133"><strong>Modo de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-134">O modo de entrada de dados do formulário.</span><span class="sxs-lookup"><span data-stu-id="cc876-134">The data entry mode for the form.</span></span> <span data-ttu-id="cc876-135">Isso se aplica apenas aos formulários abertos no modo Formulário ou no modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="cc876-135">This applies only to forms opened in Form view or Datasheet view.</span></span> <span data-ttu-id="cc876-136">Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode editar os existentes), <strong>Editar</strong> (o usuário pode editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros).</span><span class="sxs-lookup"><span data-stu-id="cc876-136">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="cc876-137">O padrão é <strong>Editar</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc876-137">The default is <strong>Edit</strong>.</span></span> <span data-ttu-id="cc876-138"><strong>Anotações</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-138"><strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="cc876-139">A <strong>configuração</strong> do argumento Modo de Dados substitui as configurações das propriedades <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>e <strong>DataEntry do</strong> formulário.</span><span class="sxs-lookup"><span data-stu-id="cc876-139">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span> <span data-ttu-id="cc876-140">For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span><span class="sxs-lookup"><span data-stu-id="cc876-140">For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="cc876-141">Se você deixar esse argumento em branco, o Access abrirá o formulário no modo de entrada de dados definido pelas propriedades <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>e <strong>DataEntry</strong> do formulário.</span><span class="sxs-lookup"><span data-stu-id="cc876-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc876-142"><strong>Modo Janela</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-143">O modo de janela no qual o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="cc876-143">The window mode in which the form opens.</span></span> <span data-ttu-id="cc876-144">Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>).</span><span class="sxs-lookup"><span data-stu-id="cc876-144">Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>).</span></span> <span data-ttu-id="cc876-145">O padrão é <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc876-145">The default is <strong>Normal</strong>.</span></span></p><p><span data-ttu-id="cc876-146"><strong>OBSERVAÇÃO:</strong>algumas <STRONG>configurações de</STRONG> argumento do Modo Janela não se aplicam ao usar documentos com guias.</span><span class="sxs-lookup"><span data-stu-id="cc876-146"><strong>NOTE</strong>: Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="cc876-147">Para alternar para janelas sobrepostas:</span><span class="sxs-lookup"><span data-stu-id="cc876-147">To switch to overlapping windows:</span></span></p>
<ol>
<li><p><span data-ttu-id="cc876-148">Clique na guia Arquivo e em <strong>Opções.</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="cc876-149">Na caixa de diálogo <strong>Opções do Access</strong>, clique em <strong>Banco de Dados Atual</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc876-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="cc876-150">Na seção <strong>Opções de Aplicativo,</strong>em <strong>Opções de Janela de Documento,</strong>clique <strong>em Sobreposição do Windows</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc876-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="cc876-151">Clique em <strong>OK</strong> e feche e abra o banco de dados novamente.</span><span class="sxs-lookup"><span data-stu-id="cc876-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cc876-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc876-152">Remarks</span></span>

<span data-ttu-id="cc876-153">Esta ação é semelhante a clicar duas vezes em um formulário no Painel de Navegação ou clicar com o botão direito do mouse no formulário no Painel de Navegação e selecionar um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="cc876-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="cc876-154">Um formulário pode ser modal (deve ser fechado ou oculto antes que o usuário possa executar qualquer outra ação) ou sem janelas (o usuário pode se mover para outras janelas enquanto o formulário estiver aberto).</span><span class="sxs-lookup"><span data-stu-id="cc876-154">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open).</span></span> <span data-ttu-id="cc876-155">Também pode ser um formulário pop-up (um formulário usado para coletar ou exibir informações que permanecem sobre todas as outras janelas do Access).</span><span class="sxs-lookup"><span data-stu-id="cc876-155">It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows).</span></span> <span data-ttu-id="cc876-156">Você pode definir **as propriedades Modal** **e PopUp** ao criar o formulário.</span><span class="sxs-lookup"><span data-stu-id="cc876-156">You set the **Modal** and **PopUp** properties when you design the form.</span></span> <span data-ttu-id="cc876-157">Se você usar **Normal** para o **argumento Modo janela,** o formulário abre no modo especificado por essas configurações de propriedade.</span><span class="sxs-lookup"><span data-stu-id="cc876-157">If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings.</span></span> <span data-ttu-id="cc876-158">Se você usar **Dialog** para o **argumento Modo Janela,** essas propriedades serão definidas como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="cc876-158">If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**.</span></span> <span data-ttu-id="cc876-159">Um formulário aberto como oculto ou como um ícone retorna ao modo especificado por suas configurações de propriedade quando você o mostra ou restaura.</span><span class="sxs-lookup"><span data-stu-id="cc876-159">A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="cc876-160">Quando você abre um formulário com o argumento **Modo** Janela definido como **Diálogo,** o Access suspende a macro até que o formulário seja fechado ou oculto.</span><span class="sxs-lookup"><span data-stu-id="cc876-160">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden.</span></span> <span data-ttu-id="cc876-161">Você pode ocultar um formulário definindo **sua propriedade Visible** como **Não** usando a **ação SetValue.**</span><span class="sxs-lookup"><span data-stu-id="cc876-161">You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>

> [!TIP]
> <span data-ttu-id="cc876-162">Você pode selecionar um formulário no Painel de Navegação e arrastá-lo para uma linha de ação de macro.</span><span class="sxs-lookup"><span data-stu-id="cc876-162">You can select a form in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="cc876-163">This automatically creates an **OpenForm** action that opens the form in Form view.</span><span class="sxs-lookup"><span data-stu-id="cc876-163">This automatically creates an **OpenForm** action that opens the form in Form view.</span></span>

<span data-ttu-id="cc876-164">O filtro e a condição WHERE aplicados tornam-se a definição da propriedade **Filter do** formulário.</span><span class="sxs-lookup"><span data-stu-id="cc876-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="cc876-165">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cc876-165">Examples</span></span>

<span data-ttu-id="cc876-166">**Definir o valor de um controle, usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="cc876-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="cc876-167">A macro a seguir abre o formulário Adicionar Produtos de um botão no formulário de Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="cc876-167">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="cc876-168">Mostra o uso das ações **Echo**, **CloseWindow**, **OpenForm**, **SetValue** e **GoToControl**.</span><span class="sxs-lookup"><span data-stu-id="cc876-168">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="cc876-169">A **ação SetValue** define o controle de ID do Fornecedor no formulário Produtos para o fornecedor atual no formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="cc876-169">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="cc876-170">A **ação IrParaControle** move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto.</span><span class="sxs-lookup"><span data-stu-id="cc876-170">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="cc876-171">Essa macro deve estar anexada ao botão Adicionar Produtos no formulário de Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="cc876-171">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc876-172">Ação</span><span class="sxs-lookup"><span data-stu-id="cc876-172">Action</span></span></p></th>
<th><p><span data-ttu-id="cc876-173">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="cc876-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="cc876-174">Comentário</span><span class="sxs-lookup"><span data-stu-id="cc876-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc876-175"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-176"><strong>Echo On</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-177">Interrompe a atualização de tela quando a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="cc876-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc876-178"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-180">Fecha o Formulário de Lista de Produtos.</span><span class="sxs-lookup"><span data-stu-id="cc876-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc876-181"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-183">Abre o formulário de produtos.</span><span class="sxs-lookup"><span data-stu-id="cc876-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc876-184"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="cc876-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="cc876-186">De definir o controle de ID de fornecedor para o fornecedor atual no formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="cc876-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc876-187"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-188"><strong>Control Name</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="cc876-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="cc876-189">Vá para o controle de ID da categoria.</span><span class="sxs-lookup"><span data-stu-id="cc876-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc876-190">A macro a seguir abre um formulário de Lista de Produtos no canto inferior direito do formulário Fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="cc876-190">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="cc876-191">Ele mostra o uso das ações **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm** e **MoveAndSizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="cc876-191">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="cc876-192">Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl** e **StopMacro.**</span><span class="sxs-lookup"><span data-stu-id="cc876-192">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="cc876-193">Essa macro deve ser anexada ao botão Revisar Produtos no formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="cc876-193">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="cc876-194">**Sincronizar formulários usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="cc876-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc876-195">Condition</span><span class="sxs-lookup"><span data-stu-id="cc876-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="cc876-196">Ação</span><span class="sxs-lookup"><span data-stu-id="cc876-196">Action</span></span></p></th>
<th><p><span data-ttu-id="cc876-197">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="cc876-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="cc876-198">Comentário</span><span class="sxs-lookup"><span data-stu-id="cc876-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="cc876-199"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-200"><strong>Echo On</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-201">Interrompe a atualização de tela quando a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="cc876-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc876-202">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="cc876-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="cc876-203"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-204"><strong>Mensagem:</strong>vá para o registro do fornecedor cujos produtos você deseja ver e clique no botão Revisar Produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="cc876-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="cc876-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span><span class="sxs-lookup"><span data-stu-id="cc876-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="cc876-206">Se não houver fornecedor atual no formulário Fornecedores, exibe uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="cc876-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc876-207">...</span><span class="sxs-lookup"><span data-stu-id="cc876-207">...</span></span></p></td>
<td><p><span data-ttu-id="cc876-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-209"><strong>Nome do controle</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="cc876-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="cc876-210">Mova o foco para o controle CompanyName.</span><span class="sxs-lookup"><span data-stu-id="cc876-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc876-211">...</span><span class="sxs-lookup"><span data-stu-id="cc876-211">...</span></span></p></td>
<td><p><span data-ttu-id="cc876-212"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="cc876-213">Pare a macro.</span><span class="sxs-lookup"><span data-stu-id="cc876-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="cc876-214"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-215"><strong>Nome do formulário</strong>: Exibição de Lista <strong>de</strong>Produtos : <strong>Nome do Filtro de</strong>Folha de Dados : <strong>Condição</strong>Onde : [SupplierID] = [Forms]! [Fornecedores]! [SupplierID] <strong>Modo de Dados</strong>: <strong>Ler Modo Somente Janela</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-216">Abra o formulário Lista de Produtos e mostre os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="cc876-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="cc876-217"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="cc876-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="cc876-218"><strong>À</strong>direita: 0,7799 &quot; <strong>para baixo:</strong>1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="cc876-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="cc876-219">Posiciona o formulário Lista de Produtos no canto inferior direito do formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="cc876-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

