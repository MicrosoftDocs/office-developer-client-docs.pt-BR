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
# <a name="openform-macro-action"></a><span data-ttu-id="f4490-102">Ação da macro AbrirFormulário</span><span class="sxs-lookup"><span data-stu-id="f4490-102">OpenForm macro action</span></span>

<span data-ttu-id="f4490-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4490-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4490-104">Você pode usar a ação **AbrirFormulário** para abrir um formulário no modo formulário, modo de design, visualização de impressão ou modo folha de de formulários.</span><span class="sxs-lookup"><span data-stu-id="f4490-104">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view.</span></span> <span data-ttu-id="f4490-105">Você pode selecionar a entrada de dados e os modos de janela para o formulário e restringir os registros que o formulário exibe.</span><span class="sxs-lookup"><span data-stu-id="f4490-105">You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="f4490-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="f4490-106">Setting</span></span>

<span data-ttu-id="f4490-107">A ação **AbrirFormulário** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f4490-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4490-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="f4490-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f4490-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4490-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4490-110"><strong>Nome do formulário</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-111">O nome do formulário a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="f4490-111">The name of the form to open.</span></span> <span data-ttu-id="f4490-112">A caixa <strong>nome do formulário</strong> na seção argumentos da <strong>ação</strong> do painel Construtor de macros mostra todos os formulários no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="f4490-112">The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database.</span></span> <span data-ttu-id="f4490-113">É um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f4490-113">This is a required argument.</span></span> <span data-ttu-id="f4490-114">Se você executar uma macro que contém a ação <strong>AbrirFormulário</strong> em um banco de dados biblioteca, o Microsoft Access procurará o formulário com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="f4490-114">If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4490-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-116">O modo de exibição no qual o formulário será aberto.</span><span class="sxs-lookup"><span data-stu-id="f4490-116">The view in which the form will open.</span></span> <span data-ttu-id="f4490-117">Clique em <strong>formulário</strong>, <strong>design</strong>, <strong>Visualizar impressão</strong>, <strong>folha</strong>de data, <strong>tabela dinâmica</strong>ou <strong>gráfico dinâmico</strong> na caixa <strong>modo de exibição</strong> .</span><span class="sxs-lookup"><span data-stu-id="f4490-117">Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="f4490-118">O padrão é <strong>Form</strong>.</span><span class="sxs-lookup"><span data-stu-id="f4490-118">The default is <strong>Form</strong>.</span></span></p><p><span data-ttu-id="f4490-119"><strong>Observação</strong>: a configuração do argumento <STRONG>Exibir</STRONG> substitui as configurações das propriedades <STRONG>ModoPadrão</STRONG> e <STRONG>ModosPermitidos</STRONG> do formulário.</span><span class="sxs-lookup"><span data-stu-id="f4490-119"><strong>NOTE</strong>: The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties.</span></span> <span data-ttu-id="f4490-120">Por exemplo, se a propriedade <STRONG>ModosPermitidos</STRONG> de um formulário estiver definida como <STRONG>folha</STRONG>de a, você ainda poderá usar a ação <STRONG>AbrirFormulário</STRONG> para abrir o formulário no modo formulário.</span><span class="sxs-lookup"><span data-stu-id="f4490-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4490-121"><strong>Nome do Filtro</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-122">Um filtro que restringe ou classifica os registros do formulário.</span><span class="sxs-lookup"><span data-stu-id="f4490-122">A filter that restricts or sorts the form's records.</span></span> <span data-ttu-id="f4490-123">Você pode digitar o nome de uma consulta existente ou de um filtro que foi salvo como consulta.</span><span class="sxs-lookup"><span data-stu-id="f4490-123">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="f4490-124">No enTanto, a consulta deve incluir todos os campos no formulário que você está abrindo ou ter a propriedade <strong>OutputAllFields</strong> definida como <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="f4490-124">However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4490-125"><strong>Condição Where</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-126">Uma cláusula SQL WHERE válida (sem a palavra WHERE) ou expressão que o Access usa para selecionar registros da tabela ou consulta base do formulário.</span><span class="sxs-lookup"><span data-stu-id="f4490-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="f4490-127">Se você selecionar um filtro com o argumento <strong>Nome do Filtro</strong>, o Access aplicará essa cláusula WHERE aos resultados do filtro.</span><span class="sxs-lookup"><span data-stu-id="f4490-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="f4490-128">Para abrir um formulário e restringir seus registros aos especificados pelo valor de um controle em outro formulário, use a seguinte expressão: <strong>[</strong><em>FieldName</em><strong>] = Forms! [</strong> <em>FormName</em> <strong>]! [</strong><em>ControlName em outro formulário</em><strong>]</strong> substitui <em>FieldName</em> pelo nome de um campo na tabela ou consulta base do formulário que você deseja abrir.</span><span class="sxs-lookup"><span data-stu-id="f4490-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="f4490-129">Substitua <em>FormName</em> e <em>ControlName em outro formulário</em> com o nome do outro formulário e o controle no outro formulário que contém o valor que você deseja que os registros no primeiro formulário correspondam.</span><span class="sxs-lookup"><span data-stu-id="f4490-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p><p><span data-ttu-id="f4490-130"><strong>Observação</strong>: o comprimento máximo do argumento <STRONG>condição onde</STRONG> é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4490-130"><strong>NOTE</strong>: The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters.</span></span> <span data-ttu-id="f4490-131">Se você precisar inserir uma cláusula SQL WHERE mais complexa e maior que isso, use o método <STRONG>OpenForm</STRONG> do objeto <STRONG>DoCmd</STRONG> em um módulo do Visual Basic for Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="f4490-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="f4490-132">É possível inserir instruções de cláusulas SQL WHERE de até 32.768 caracteres no VBA.</span><span class="sxs-lookup"><span data-stu-id="f4490-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4490-133"><strong>Modo de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-134">O modo de entrada de dados do formulário.</span><span class="sxs-lookup"><span data-stu-id="f4490-134">The data entry mode for the form.</span></span> <span data-ttu-id="f4490-135">Isso se aplica apenas aos formulários abertos no modo Formulário ou no modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="f4490-135">This applies only to forms opened in Form view or Datasheet view.</span></span> <span data-ttu-id="f4490-136">Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode editar os existentes), <strong>Editar</strong> (o usuário pode editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros).</span><span class="sxs-lookup"><span data-stu-id="f4490-136">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="f4490-137">O padrão é <strong>Editar</strong>.</span><span class="sxs-lookup"><span data-stu-id="f4490-137">The default is <strong>Edit</strong>.</span></span> <span data-ttu-id="f4490-138"><strong>Anotações</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-138"><strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="f4490-139">A configuração do argumento <strong>modo de dados</strong> substitui as configurações das propriedades <strong>PermitirEdições</strong>, <strong>PermitirExclusões</strong>, <strong>PermitirAdições</strong>e DataEntry do formulário. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="f4490-139">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span> <span data-ttu-id="f4490-140">Por exemplo, se a propriedade <strong>PermitirEdições</strong> de um formulário estiver definida como <strong>não</strong>, você ainda poderá usar a ação <strong>AbrirFormulário</strong> para abrir o formulário no modo de edição.</span><span class="sxs-lookup"><span data-stu-id="f4490-140">For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="f4490-141">Se você deixar este argumento em branco, o Access abrirá o formulário no modo de entrada de dados definido pelas propriedades <strong>PermitirEdições</strong>, <strong>PermitirExclusões</strong>, <strong>PermitirAdições</strong>e DataEntry do formulário. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="f4490-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4490-142"><strong>Modo Janela</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-143">O modo de janela em que o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="f4490-143">The window mode in which the form opens.</span></span> <span data-ttu-id="f4490-144">Clique em <strong>normal</strong> (o formulário é aberto no modo definido por suas propriedades) <strong>, oculto</strong> (o formulário é oculto), <strong>ícone</strong> (o formulário abre minimizado como uma pequena barra de título na parte inferior da tela) ou <strong>caixa de diálogo</strong> (a <strong>janela restrita</strong> e o <strong>pop-up do formulário </strong>propriedades estão definidas como <strong>Sim</strong>).</span><span class="sxs-lookup"><span data-stu-id="f4490-144">Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>).</span></span> <span data-ttu-id="f4490-145">O padrão é <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="f4490-145">The default is <strong>Normal</strong>.</span></span></p><p><span data-ttu-id="f4490-146"><strong>Observação</strong>: algumas configurações de argumento do <STRONG>modo de janela</STRONG> não se aplicam ao usar documentos com guias.</span><span class="sxs-lookup"><span data-stu-id="f4490-146"><strong>NOTE</strong>: Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="f4490-147">Para alternar para janelas sobrepostas:</span><span class="sxs-lookup"><span data-stu-id="f4490-147">To switch to overlapping windows:</span></span></p>
<ol>
<li><p><span data-ttu-id="f4490-148">Clique na guia arquivo e em <strong>Opções</strong>.</span><span class="sxs-lookup"><span data-stu-id="f4490-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f4490-149">Na caixa de diálogo <strong>Opções do Access</strong>, clique em <strong>Banco de Dados Atual</strong>.</span><span class="sxs-lookup"><span data-stu-id="f4490-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f4490-150">Na seção <strong>Opções do aplicativo</strong>, em <strong>Opções da janela de documento</strong>, clique em janelas sobrepostas. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="f4490-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f4490-151">Clique em <strong>OK</strong> e feche e abra o banco de dados novamente.</span><span class="sxs-lookup"><span data-stu-id="f4490-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f4490-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4490-152">Remarks</span></span>

<span data-ttu-id="f4490-153">Esta ação é semelhante a clicar duas vezes em um formulário no painel de navegação ou clicar com o botão direito do mouse no formulário no painel de navegação e selecionar um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="f4490-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="f4490-154">Um formulário pode ser de janela restrita (deve ser fechado ou oculto para que o usuário possa executar qualquer outra ação) ou sem janela restrita (o usuário pode mover para outras janelas enquanto o formulário está aberto).</span><span class="sxs-lookup"><span data-stu-id="f4490-154">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open).</span></span> <span data-ttu-id="f4490-155">Também pode ser um formulário pop-up (um formulário usado para coletar ou exibir informações que permanecem na parte superior de todas as outras janelas do Access).</span><span class="sxs-lookup"><span data-stu-id="f4490-155">It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows).</span></span> <span data-ttu-id="f4490-156">Você define as propriedades **modal** e **Popup** quando cria o formulário.</span><span class="sxs-lookup"><span data-stu-id="f4490-156">You set the **Modal** and **PopUp** properties when you design the form.</span></span> <span data-ttu-id="f4490-157">Se você usar **normal** para o argumento **modo janela** , o formulário é aberto no modo especificado por essas configurações de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f4490-157">If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings.</span></span> <span data-ttu-id="f4490-158">Se você usar a **caixa de diálogo** do argumento **modo janela** , essas propriedades serão definidas como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="f4490-158">If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**.</span></span> <span data-ttu-id="f4490-159">Um formulário aberto como oculto ou como um ícone retorna ao modo especificado por suas configurações de propriedade quando você o exibe ou restaura.</span><span class="sxs-lookup"><span data-stu-id="f4490-159">A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="f4490-160">Quando você abre um formulário com o argumento **modo janela** definido como **caixa de diálogo**, o Access suspende a macro até que o formulário seja fechado ou oculto.</span><span class="sxs-lookup"><span data-stu-id="f4490-160">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden.</span></span> <span data-ttu-id="f4490-161">Você pode ocultar um formulário definindo sua propriedade **Visible** como **não** usando a ação **DefinirValor** .</span><span class="sxs-lookup"><span data-stu-id="f4490-161">You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>

> [!TIP]
> <span data-ttu-id="f4490-162">Você pode selecionar um formulário no painel de navegação e arrastá-lo para uma linha de ação de macro.</span><span class="sxs-lookup"><span data-stu-id="f4490-162">You can select a form in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="f4490-163">Isso cria automaticamente uma ação **AbrirFormulário** que abre o formulário no modo formulário.</span><span class="sxs-lookup"><span data-stu-id="f4490-163">This automatically creates an **OpenForm** action that opens the form in Form view.</span></span>

<span data-ttu-id="f4490-164">O filtro e a condição WHERE aplicados tornam-se a configuração da propriedade **Filter** do formulário.</span><span class="sxs-lookup"><span data-stu-id="f4490-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="f4490-165">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f4490-165">Examples</span></span>

<span data-ttu-id="f4490-166">**Definir o valor de um controle usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="f4490-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="f4490-167">A macro a seguir abre o formulário Adicionar produtos a partir de um botão no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="f4490-167">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="f4490-168">Ela mostra o uso das ações **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **IrParaControle** .</span><span class="sxs-lookup"><span data-stu-id="f4490-168">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="f4490-169">A ação **DefinirValor** define o controle de ID do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="f4490-169">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="f4490-170">A ação **IrParaControle** move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto.</span><span class="sxs-lookup"><span data-stu-id="f4490-170">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="f4490-171">Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="f4490-171">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4490-172">Ação</span><span class="sxs-lookup"><span data-stu-id="f4490-172">Action</span></span></p></th>
<th><p><span data-ttu-id="f4490-173">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="f4490-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="f4490-174">Comentário</span><span class="sxs-lookup"><span data-stu-id="f4490-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4490-175"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-176"><strong>Echo ativado</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-177">Interrompa a atualização da tela enquanto a macro estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="f4490-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4490-178"><strong>FecharJanela</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-179"><strong>Tipo de objeto</strong>: <strong>nome</strong>do formObject: <strong>salvamento</strong>da lista de produtos: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-180">Feche o formulário lista de produtos.</span><span class="sxs-lookup"><span data-stu-id="f4490-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4490-181"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-182"><strong>Nome do formulário</strong>: modo de <strong>exibição</strong>de produtos: <strong>modo FormData</strong>: <strong>modo AddWindow</strong>: <strong>normal</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-183">Abra o formulário produtos.</span><span class="sxs-lookup"><span data-stu-id="f4490-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4490-184"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-185"><strong>Item</strong>: [formulários]! [Produtos]! [CódigoDoFornecedor] <strong>Expressão</strong>: CódigoDoFornecedor</span><span class="sxs-lookup"><span data-stu-id="f4490-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="f4490-186">Defina o controle de ID do fornecedor como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="f4490-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4490-187"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-188"><strong>Nome do controle</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="f4490-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="f4490-189">Vá para o controle de ID de categoria.</span><span class="sxs-lookup"><span data-stu-id="f4490-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f4490-190">A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="f4490-190">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="f4490-191">Ela mostra o uso das ações **eco**, **MessageBox**, **IrParaControle**, **PararMacro**, **AbrirFormulário**e **moveredimensionarjanela** .</span><span class="sxs-lookup"><span data-stu-id="f4490-191">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="f4490-192">Também mostra o uso de uma expressão condicional com as ações **MessageBox**, **IrParaControle**e **PararMacro** .</span><span class="sxs-lookup"><span data-stu-id="f4490-192">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="f4490-193">Essa macro deve ser anexada ao botão reVisar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="f4490-193">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="f4490-194">**Sincronizar formulários usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="f4490-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4490-195">Condição</span><span class="sxs-lookup"><span data-stu-id="f4490-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="f4490-196">Ação</span><span class="sxs-lookup"><span data-stu-id="f4490-196">Action</span></span></p></th>
<th><p><span data-ttu-id="f4490-197">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="f4490-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="f4490-198">Comentário</span><span class="sxs-lookup"><span data-stu-id="f4490-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="f4490-199"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-200"><strong>Echo ativado</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-201">Interrompa a atualização da tela enquanto a macro estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="f4490-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4490-202">Énulo ([CódigoDoFornecedor])</span><span class="sxs-lookup"><span data-stu-id="f4490-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="f4490-203"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-204"><strong>Mensagem</strong>: mova para o registro de fornecedor cujos produtos você deseja ver e, em seguida, clique no botão revisar produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="f4490-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="f4490-205"><strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecionar um fornecedor</span><span class="sxs-lookup"><span data-stu-id="f4490-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="f4490-206">Se não houver um fornecedor atual no formulário fornecedores, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f4490-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4490-207">...</span><span class="sxs-lookup"><span data-stu-id="f4490-207"></span></span></p></td>
<td><p><span data-ttu-id="f4490-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-209"><strong>Nome do controle</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="f4490-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="f4490-210">Mover o foco para o controle CompanyName.</span><span class="sxs-lookup"><span data-stu-id="f4490-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4490-211">...</span><span class="sxs-lookup"><span data-stu-id="f4490-211"></span></span></p></td>
<td><p><span data-ttu-id="f4490-212"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f4490-213">Interrompa a macro.</span><span class="sxs-lookup"><span data-stu-id="f4490-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="f4490-214"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-215"><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>de lista de produtos: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [CódigoDoFornecedor] = [formulários]! [Fornecedores]! [CódigoDoFornecedor] <strong>Modo de dados</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>normal</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-216">Abra o formulário lista de produtos e mostre os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="f4490-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="f4490-217"><strong>Moveredimensionarjanela</strong></span><span class="sxs-lookup"><span data-stu-id="f4490-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="f4490-218"><strong>direita</strong>: 0,7799&quot; <strong>baixo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="f4490-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="f4490-219">Posicione o formulário lista de produtos no canto inferior direito do formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="f4490-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

