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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707623"
---
# <a name="openform-macro-action"></a><span data-ttu-id="ef5ff-102">Ação da macro AbrirFormulário</span><span class="sxs-lookup"><span data-stu-id="ef5ff-102">OpenForm macro action</span></span>

<span data-ttu-id="ef5ff-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef5ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef5ff-104">Você pode usar a ação **AbrirFormulário** para abrir um formulário no modo formulário, modo de Design, modo Visualizar impressão ou modo folha de dados.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-104">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view.</span></span> <span data-ttu-id="ef5ff-105">Você pode selecionar a entrada de dados e os modos de janela para o formulário e restringir os registros que o formulário exibe.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-105">You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="ef5ff-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="ef5ff-106">Setting</span></span>

<span data-ttu-id="ef5ff-107">A ação **AbrirFormulário** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef5ff-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="ef5ff-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ef5ff-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef5ff-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef5ff-110"><strong>Nome do formulário</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-111">O nome do formulário a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-111">The name of the form to open.</span></span> <span data-ttu-id="ef5ff-112">Caixa <strong>Nome do formulário</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todos os formulários no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-112">The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database.</span></span> <span data-ttu-id="ef5ff-113">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-113">This is a required argument.</span></span> <span data-ttu-id="ef5ff-114">Se você executar uma macro que contém a ação <strong>AbrirFormulário</strong> em um banco de dados biblioteca, o Microsoft Access procurará primeiro o formulário com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-114">If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5ff-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-116">O modo de exibição no qual o formulário será aberto.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-116">The view in which the form will open.</span></span> <span data-ttu-id="ef5ff-117">Clique em <strong>formulário</strong>, <strong>Design</strong>, <strong>Modo Visualizar impressão</strong>, <strong>folha de dados</strong>, <strong>tabela dinâmica</strong>ou <strong>gráfico dinâmico</strong> , na caixa <strong>Exibir</strong> .</span><span class="sxs-lookup"><span data-stu-id="ef5ff-117">Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="ef5ff-118">O padrão é <strong>formulário</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-118">The default is <strong>Form</strong>.</span></span></p><p><span data-ttu-id="ef5ff-119"><strong>Observação</strong>: A configuração do argumento <STRONG>modo de exibição</STRONG> substitui as configurações das propriedades de <STRONG>ModoPadrão</STRONG> e <STRONG>ViewsAllowed</STRONG> do formulário.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-119"><strong>NOTE</strong>: The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties.</span></span> <span data-ttu-id="ef5ff-120">Por exemplo, se a propriedade <STRONG>ViewsAllowed</STRONG> de um formulário é definida como <STRONG>folha de dados</STRONG>, você ainda pode usar a ação <STRONG>AbrirFormulário</STRONG> para abrir o formulário no modo formulário.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5ff-121"><strong>Nome do Filtro</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-122">Um filtro que restringe ou classifica os registros do formulário.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-122">A filter that restricts or sorts the form's records.</span></span> <span data-ttu-id="ef5ff-123">Você pode inserir o nome de uma consulta existente ou um filtro que foi salvo como uma consulta.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-123">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="ef5ff-124">No entanto, a consulta deve incluir todos os campos do formulário que você está abrindo ou ter sua propriedade <strong>OutputAllFields</strong> definida como <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-124">However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5ff-125"><strong>Condição Where</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-126">Uma cláusula SQL WHERE válida (sem a palavra onde) ou expressão que o Access utiliza para selecionar registros do formulário da tabela ou consulta base.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="ef5ff-127">Se você selecionar um filtro com o argumento <strong>Nome do filtro</strong> , o Access aplica essa cláusula WHERE aos resultados do filtro.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="ef5ff-128">Para abrir um formulário e restringir seus registros àqueles especificados pelo valor de um controle em outro formulário, use a seguinte expressão: <strong>[</strong><em>fieldname</em><strong>] = formulários! [</strong> <em>formname</em> <strong>]! [</strong><em>controlname em outro formulário</em><strong>]</strong> substitua <em>fieldname</em> pelo nome de um campo na tabela ou consulta do formulário que você deseja abrir subjacente.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="ef5ff-129">Substitua o nome de outro formulário e o controle no outro formulário que contém o valor que você deseja que os registros no primeiro formulário devem corresponder <em>formname</em> e <em>controlname em outro formulário</em> .</span><span class="sxs-lookup"><span data-stu-id="ef5ff-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p><p><span data-ttu-id="ef5ff-130"><strong>Observação</strong>: O comprimento máximo do argumento <STRONG>Condição Where</STRONG> é 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-130"><strong>NOTE</strong>: The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters.</span></span> <span data-ttu-id="ef5ff-131">Se você precisar inserir uma cláusula SQL WHERE complexa mais, maior que isso, use o método <STRONG>OpenForm</STRONG> do objeto <STRONG>DoCmd</STRONG> no Visual Basic para módulo Applications (VBA) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="ef5ff-132">Você pode inserir instruções cláusula SQL WHERE de até 32.768 caracteres no VBA.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5ff-133"><strong>Modo de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-134">O modo de entrada de dados para o formulário.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-134">The data entry mode for the form.</span></span> <span data-ttu-id="ef5ff-135">Isso se aplica apenas aos formulários abertos no modo Formulário ou no modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-135">This applies only to forms opened in Form view or Datasheet view.</span></span> <span data-ttu-id="ef5ff-136">Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros mas não pode editar registros existentes), <strong>Editar</strong> (o usuário pode editar registros existentes e adicionar novos registros), ou <strong>Somente leitura</strong> (o usuário só pode exibir registros).</span><span class="sxs-lookup"><span data-stu-id="ef5ff-136">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="ef5ff-137">O padrão é <strong>Editar</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-137">The default is <strong>Edit</strong>.</span></span> <span data-ttu-id="ef5ff-138"><strong>Anotações</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-138"><strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="ef5ff-139">A definição do argumento <strong>Modo de dados</strong> substitui as configurações das propriedades de <strong>PermitirEdições</strong>, <strong>PermitirExclusões</strong>, <strong>PermitirAdições</strong>e <strong>DataEntry</strong> do formulário.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-139">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span> <span data-ttu-id="ef5ff-140">Por exemplo, se uma propriedade <strong>PermitirEdições</strong> formulário for definida como <strong>não</strong>, você ainda pode usar a ação <strong>AbrirFormulário</strong> para abrir o formulário no modo de edição.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-140">For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="ef5ff-141">Se você deixar este argumento em branco, o Access abre o formulário no modo de entrada de dados definido pelas propriedades de <strong>PermitirEdições</strong>, <strong>PermitirExclusões</strong>, <strong>PermitirAdições</strong>e <strong>DataEntry</strong> do formulário.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5ff-142"><strong>Modo Janela</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-143">O modo de janela na qual o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-143">The window mode in which the form opens.</span></span> <span data-ttu-id="ef5ff-144">Clique em <strong>Normal</strong> (o formulário é aberto no modo definido pelas suas propriedades), <strong>oculto</strong> (o formulário é oculto), o <strong>ícone</strong> (o formulário é aberto minimizado como uma pequena barra de título na parte inferior da tela), ou <strong>diálogo</strong> (do formulário <strong>Modal</strong> e PopUp do <strong> </strong>propriedades são definidas como <strong>Sim</strong>).</span><span class="sxs-lookup"><span data-stu-id="ef5ff-144">Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>).</span></span> <span data-ttu-id="ef5ff-145">O padrão é <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-145">The default is <strong>Normal</strong>.</span></span></p><p><span data-ttu-id="ef5ff-146"><strong>Observação</strong>: algumas configurações do argumento <STRONG>Modo janela</STRONG> não se aplicam ao uso de documentos com abas.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-146"><strong>NOTE</strong>: Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="ef5ff-147">Para alternar para janelas sobrepostas:</span><span class="sxs-lookup"><span data-stu-id="ef5ff-147">To switch to overlapping windows:</span></span></p>
<ol>
<li><p><span data-ttu-id="ef5ff-148">Clique na guia arquivo e clique em <strong>Opções</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="ef5ff-149">Na caixa de diálogo <strong>Opções do Access</strong> , clique em <strong>Banco de dados atual</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="ef5ff-150">Na seção <strong>Opções de aplicativo</strong>, em <strong>Opções da janela de documento</strong>, clique em <strong>Janelas sobrepostas</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="ef5ff-151">Clique em <strong>OK</strong> e feche e abra o banco de dados novamente.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ef5ff-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef5ff-152">Remarks</span></span>

<span data-ttu-id="ef5ff-153">Esta ação é semelhante a clicar duas vezes em um formulário no painel de navegação, ou clicando o formulário no painel de navegação e selecionando um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="ef5ff-154">Um formulário pode ser modal (deve ser fechado ou oculto para que o usuário possa realizar qualquer outra ação) ou sem janela restrita (o usuário pode mover para outras janelas enquanto o formulário está aberto).</span><span class="sxs-lookup"><span data-stu-id="ef5ff-154">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open).</span></span> <span data-ttu-id="ef5ff-155">Ele também pode ser um formulário pop-up (um formulário utilizado para reunir ou exibir informações que permanecem na parte superior de todas as outras janelas do Access).</span><span class="sxs-lookup"><span data-stu-id="ef5ff-155">It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows).</span></span> <span data-ttu-id="ef5ff-156">Você definir as propriedades **Modal** e **PopUp** quando você cria o formulário.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-156">You set the **Modal** and **PopUp** properties when you design the form.</span></span> <span data-ttu-id="ef5ff-157">Se você usar **Normal** para o argumento **Modo janela** , o formulário é aberto no modo especificado pelas configurações dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-157">If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings.</span></span> <span data-ttu-id="ef5ff-158">Se você usar a **caixa de diálogo** do argumento **Modo janela** , duas essas propriedades serão definidas como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-158">If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**.</span></span> <span data-ttu-id="ef5ff-159">Um formulário aberto como oculto ou como um ícone retorna ao modo especificado por suas configurações de propriedade quando você mostra ou restaurá-lo.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-159">A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="ef5ff-160">Quando você abre um formulário com o argumento **Modo janela** definido como **diálogo**, o Access suspende a macro até que o formulário é fechado ou oculto.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-160">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden.</span></span> <span data-ttu-id="ef5ff-161">Você pode ocultar um formulário definindo sua propriedade **Visible** como **não** usando a ação **DefinirValor** .</span><span class="sxs-lookup"><span data-stu-id="ef5ff-161">You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>

> [!TIP]
> <span data-ttu-id="ef5ff-162">Você pode selecionar um formulário no painel de navegação e arraste-o para uma linha de ação de macro.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-162">You can select a form in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="ef5ff-163">Isso cria automaticamente uma ação **AbrirFormulário** que abre o formulário no modo formulário.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-163">This automatically creates an **OpenForm** action that opens the form in Form view.</span></span>

<span data-ttu-id="ef5ff-164">O filtro e a condição WHERE aplicados se tornam a configuração da propriedade **Filter** do formulário.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="ef5ff-165">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ef5ff-165">Examples</span></span>

<span data-ttu-id="ef5ff-166">**Definir o valor de um controle usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="ef5ff-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="ef5ff-167">A macro a seguir abre o formulário Adicionar produtos com um botão no formulário Suppliers.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-167">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="ef5ff-168">Ela mostra o uso do **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **GoToControl** ações.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-168">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="ef5ff-169">A ação **DefinirValor** define o controle de código do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-169">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="ef5ff-170">A ação **GoToControl** , em seguida, move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-170">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="ef5ff-171">Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-171">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef5ff-172">Ação</span><span class="sxs-lookup"><span data-stu-id="ef5ff-172">Action</span></span></p></th>
<th><p><span data-ttu-id="ef5ff-173">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="ef5ff-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="ef5ff-174">Comentário</span><span class="sxs-lookup"><span data-stu-id="ef5ff-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef5ff-175"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-176"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-177">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5ff-178"><strong>FecharJanela</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-179"><strong>Tipo de objeto</strong>: <strong>Nome FormObject</strong>: lista de produto para <strong>Salvar</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-180">Feche o formulário de lista de produtos.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5ff-181"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-182"><strong>Nome do formulário</strong>: produtos <strong>modo de exibição</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-183">Abra o formulário Products.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5ff-184"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-185"><strong>Item</strong>: [formulários]! [Produtos]! [SupplierID] <strong>Expressão</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="ef5ff-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="ef5ff-186">Defina o controle de código do fornecedor como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5ff-187"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-188"><strong>Nome do controle</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="ef5ff-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="ef5ff-189">Vá para o controle de ID da categoria.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef5ff-190">A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-190">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="ef5ff-191">Ela mostra o uso do **eco**, **MessageBox**, **GoToControl**, **PararMacro**, **AbrirFormulário**e **Moveredimensionarjanela** ações.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-191">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="ef5ff-192">Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl**e **PararMacro** .</span><span class="sxs-lookup"><span data-stu-id="ef5ff-192">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="ef5ff-193">Essa macro deve ser anexada ao botão Revisar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-193">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="ef5ff-194">**Sincronizar formulários usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="ef5ff-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef5ff-195">Condição</span><span class="sxs-lookup"><span data-stu-id="ef5ff-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="ef5ff-196">Ação</span><span class="sxs-lookup"><span data-stu-id="ef5ff-196">Action</span></span></p></th>
<th><p><span data-ttu-id="ef5ff-197">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="ef5ff-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="ef5ff-198">Comentário</span><span class="sxs-lookup"><span data-stu-id="ef5ff-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ef5ff-199"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-200"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-201">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5ff-202">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="ef5ff-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="ef5ff-203"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-204"><strong>Mensagem</strong>: mover para o registro do fornecedor cujos produtos você deseja ver, em seguida, clique no botão Revisar produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="ef5ff-205"><strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecione um fornecedor</span><span class="sxs-lookup"><span data-stu-id="ef5ff-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="ef5ff-206">Se não houver nenhum fornecedor atual no formulário fornecedores, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef5ff-207">...</span><span class="sxs-lookup"><span data-stu-id="ef5ff-207"></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-209"><strong>Nome do controle</strong>: NomeDaEmpresa</span><span class="sxs-lookup"><span data-stu-id="ef5ff-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="ef5ff-210">Mova o foco para o controle NomeDaEmpresa.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef5ff-211">...</span><span class="sxs-lookup"><span data-stu-id="ef5ff-211"></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-212"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ef5ff-213">Interrompa a macro.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ef5ff-214"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-215"><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>da lista de produto: <strong>DatasheetFilter nome</strong>: <strong>condição onde</strong>: [SupplierID] = [formulários]! Fornecedores! [SupplierID] <strong>Modo de dados</strong>: <strong>Modo de OnlyWindow de leitura</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-216">Abra o formulário de lista de produtos e mostram os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ef5ff-217"><strong>Moveredimensionarjanela</strong></span><span class="sxs-lookup"><span data-stu-id="ef5ff-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="ef5ff-218"><strong>Direita</strong>: 0.7799&quot; <strong>para baixo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="ef5ff-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="ef5ff-219">Posiciona o formulário de lista de produtos no canto inferior direito do formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="ef5ff-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

