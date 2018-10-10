---
title: Ação de Macro SetValue
TOCTitle: SetValue Macro Action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f845dc5512611aa948991ad2099169a25bbcb113
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462188"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="46363-102">Ação de Macro SetValue</span><span class="sxs-lookup"><span data-stu-id="46363-102">SetValue Macro Action</span></span>


<span data-ttu-id="46363-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="46363-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="46363-104">Você pode usar a ação **DefinirValor** para definir o valor de um campo do Microsoft Access, o controle ou a propriedade em um formulário, uma folha de dados do formulário ou um relatório.</span><span class="sxs-lookup"><span data-stu-id="46363-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>


> [!NOTE]
> <P><span data-ttu-id="46363-105">Você não pode usar a ação <STRONG>DefinirValor</STRONG> para definir o valor de uma propriedade que retorna um objeto do Access.</span><span class="sxs-lookup"><span data-stu-id="46363-105">You cannot use the <STRONG>SetValue</STRONG> action to set the value of an Access property that returns an object.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="46363-p101">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="46363-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="46363-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="46363-108">Setting</span></span>

<span data-ttu-id="46363-109">A ação **DefinirValor** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="46363-109">The **SetValue** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46363-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="46363-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="46363-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="46363-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46363-112"><strong>1.1</strong></span><span class="sxs-lookup"><span data-stu-id="46363-112"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-113">O nome do campo, controle ou a propriedade cujo valor você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="46363-113">The name of the field, control, or property whose value you want to set.</span></span> <span data-ttu-id="46363-114">Insira o nome de campo, controle ou propriedade na caixa de <strong>Item</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="46363-114">Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="46363-115">Você deve usar a sintaxe completa para se referir a este item, como <em>controlname</em> (para um controle no formulário ou relatório do qual a macro foi chamada) ou <strong>formulários</strong>! <em>formname</em>! <em>controlname</em>.</span><span class="sxs-lookup"><span data-stu-id="46363-115">You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>.</span></span> <span data-ttu-id="46363-116">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="46363-116">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46363-117"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="46363-117"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-118">A expressão que Access usa para definir o valor deste item.</span><span class="sxs-lookup"><span data-stu-id="46363-118">The expression Access uses to set the value for this item.</span></span> <span data-ttu-id="46363-119">Você sempre deve usar a sintaxe completa para se referir a quaisquer objetos na expressão.</span><span class="sxs-lookup"><span data-stu-id="46363-119">You must always use the full syntax to refer to any objects in the expression.</span></span> <span data-ttu-id="46363-120">Por exemplo, para aumentar o valor em um controle salário em um formulário Employees em 10 por cento, use Forms! Funcionários! Salário \* 1.1.</span><span class="sxs-lookup"><span data-stu-id="46363-120">For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1.</span></span> <span data-ttu-id="46363-121">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="46363-121">This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="46363-122">Você não deve usar um sinal de igualdade (<STRONG>=</STRONG>) antes da expressão neste argumento.</span><span class="sxs-lookup"><span data-stu-id="46363-122">You shouldn't use an equal sign (<STRONG>=</STRONG>) before the expression in this argument.</span></span> <span data-ttu-id="46363-123">Se fizer isso, o Access avalia a expressão e, em seguida, usa esse valor como a expressão neste argumento.</span><span class="sxs-lookup"><span data-stu-id="46363-123">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="46363-124">Isso pode gerar resultados inesperados se a expressão for uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="46363-124">This can produce unexpected results if the expression is a string.</span></span></P>


<p><span data-ttu-id="46363-125">Por exemplo, se você digitar <strong> = &quot;sequência1&quot; </strong> para este argumento, o Access primeiro avalia a expressão como Sequência1.</span><span class="sxs-lookup"><span data-stu-id="46363-125">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="46363-126">Em seguida, ele usa String1 como a expressão neste argumento, esperando encontrar um controle ou a propriedade chamada String1 no formulário ou relatório que chamou a macro.</span><span class="sxs-lookup"><span data-stu-id="46363-126">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="46363-127">Em um banco de dados do Access (. mdb ou. accdb), clique no botão <STRONG>Construir</STRONG> para usar o construtor de expressões para criar uma expressão para um desses argumentos.</span><span class="sxs-lookup"><span data-stu-id="46363-127">In an Access database (.mdb or .accdb), click the <STRONG>Build</STRONG> button to use the Expression Builder to create an expression for either of these arguments.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="46363-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="46363-128">Remarks</span></span>

<span data-ttu-id="46363-129">Você pode usar esta ação para definir um valor para um campo ou controle em um formulário, uma folha de dados do formulário ou um relatório.</span><span class="sxs-lookup"><span data-stu-id="46363-129">You can use this action to set a value for a field or control on a form, a form datasheet, or a report.</span></span> <span data-ttu-id="46363-130">Você também pode definir o valor para quase todas as propriedades do relatório, formulário e controle em qualquer modo.</span><span class="sxs-lookup"><span data-stu-id="46363-130">You can also set the value for almost all control, form, and report properties in any view.</span></span> <span data-ttu-id="46363-131">Para descobrir se uma determinada propriedade pode ser definida usando uma macro e quais modos de exibição pode ser definida, consulte o tópico de ajuda para essa propriedade no Editor do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="46363-131">To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="46363-132">Você também pode definir o valor de um campo na tabela de base de um formulário, mesmo se o formulário não contiver um controle acoplado ao campo.</span><span class="sxs-lookup"><span data-stu-id="46363-132">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="46363-133">Use a sintaxe **formulários**\!*formname*\!*fieldname* na caixa de **Item** para definir o valor desse campo.</span><span class="sxs-lookup"><span data-stu-id="46363-133">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="46363-134">Você também pode consultar a um campo da tabela base de um relatório usando a sintaxe **relatórios**\!*reportname*\!*fieldname*, mas deve haver um controle no relatório acoplado a esse campo ou o campo deve ser referido em um controle calculado no relatório.</span><span class="sxs-lookup"><span data-stu-id="46363-134">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="46363-135">Se você definir o valor de um controle em um formulário, a ação **DefinirValor** não aciona as regras de validação de nível de formulário do controle, mas ela acionará as regras de validação de nível de tabela do campo base se o controle é um controle acoplado.</span><span class="sxs-lookup"><span data-stu-id="46363-135">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control.</span></span> <span data-ttu-id="46363-136">A ação **DefinirValor** também aciona o recálculo, mas o recálculo pode não acontecer imediatamente.</span><span class="sxs-lookup"><span data-stu-id="46363-136">The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately.</span></span> <span data-ttu-id="46363-137">Para acionar um redesenho imediato e forçar a conclusão do recálculo, use a ação **RedesenharObjeto** .</span><span class="sxs-lookup"><span data-stu-id="46363-137">To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action.</span></span> <span data-ttu-id="46363-138">O valor definido em um controle usando a ação **DefinirValor** também não é afetado por uma máscara de entrada definida do controle ou propriedade de **máscara de entrada** do campo de base.</span><span class="sxs-lookup"><span data-stu-id="46363-138">The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="46363-139">Para alterar o valor de um controle, você pode usar a ação **DefinirValor** em uma macro especificada pela propriedade de evento **AfterUpdate** do controle.</span><span class="sxs-lookup"><span data-stu-id="46363-139">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property.</span></span> <span data-ttu-id="46363-140">No entanto, você não pode usar a ação **DefinirValor** em uma macro especificada pela propriedade de evento **BeforeUpdate** de um controle para alterar o valor do controle (embora você pode usar a ação **DefinirValor** para alterar o valor de outros controles).</span><span class="sxs-lookup"><span data-stu-id="46363-140">However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls).</span></span> <span data-ttu-id="46363-141">Você também pode usar a ação **DefinirValor** em uma macro especificada pela propriedade **BeforeUpdate** ou **AfterUpdate** de um formulário para alterar o valor de quaisquer controles no registro atual.</span><span class="sxs-lookup"><span data-stu-id="46363-141">You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>


> [!NOTE]
> <P><span data-ttu-id="46363-142">Você não pode usar a ação <STRONG>DefinirValor</STRONG> para definir o valor dos controles a seguir:</span><span class="sxs-lookup"><span data-stu-id="46363-142">You can't use the <STRONG>SetValue</STRONG> action to set the value of the following controls:</span></span></P>
> <UL>
> <LI>
> <P><span data-ttu-id="46363-143">Controles vinculados e controles calculados em relatórios.</span><span class="sxs-lookup"><span data-stu-id="46363-143">Bound controls and calculated controls on reports.</span></span></P>
> <LI>
> <P><span data-ttu-id="46363-144">Controles calculados em formulários.</span><span class="sxs-lookup"><span data-stu-id="46363-144">Calculated controls on forms.</span></span></P></LI></UL>




> [!TIP]
> <P><span data-ttu-id="46363-145">Você pode usar a ação <STRONG>DefinirValor</STRONG> para ocultar ou mostrar um formulário no modo formulário.</span><span class="sxs-lookup"><span data-stu-id="46363-145">You can use the <STRONG>SetValue</STRONG> action to hide or show a form in Form view.</span></span> <span data-ttu-id="46363-146">Insira <STRONG>Forms</STRONG>! <EM>formname</EM> <STRONG>. Visível</STRONG> na caixa de <STRONG>Item</STRONG> e <STRONG>não</STRONG> ou <STRONG>Sim</STRONG> na caixa <STRONG>expressão</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="46363-146">Enter <STRONG>Forms</STRONG>!<EM>formname</EM><STRONG>.Visible</STRONG> in the <STRONG>Item</STRONG> box and <STRONG>No</STRONG> or <STRONG>Yes</STRONG> in the <STRONG>Expression</STRONG> box.</span></span> <span data-ttu-id="46363-147">A definição da propriedade <STRONG>visível</STRONG> do formulário uma janela restrita como <STRONG>não</STRONG> oculta o formulário e o torna sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="46363-147">Setting a modal form's <STRONG>Visible</STRONG> property to <STRONG>No</STRONG> hides the form and makes it modeless.</span></span> <span data-ttu-id="46363-148">Configuração da propriedade como <STRONG>Sim</STRONG> exibe o formulário e o torna restrito novamente.</span><span class="sxs-lookup"><span data-stu-id="46363-148">Setting the property to <STRONG>Yes</STRONG> displays the form and makes it modal again.</span></span></P>



<span data-ttu-id="46363-149">Alterando o valor da ou adicionando novos dados em um controle usando a ação **DefinirValor** em uma macro não aciona eventos como **BeforeUpdate**, **BeforeInsert**ou **Change** que ocorrem quando você altera ou insere dados nesses controles através do interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="46363-149">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface.</span></span> <span data-ttu-id="46363-150">Esses eventos também não ocorrem se você definir o valor do controle usando um Visual Basic para módulo Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="46363-150">These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="46363-151">Esta ação não está disponível em um módulo do VBA.</span><span class="sxs-lookup"><span data-stu-id="46363-151">This action isn't available in a VBA module.</span></span> <span data-ttu-id="46363-152">Defina o valor diretamente no VBA.</span><span class="sxs-lookup"><span data-stu-id="46363-152">Set the value directly in VBA.</span></span>

## <a name="example"></a><span data-ttu-id="46363-153">Exemplo</span><span class="sxs-lookup"><span data-stu-id="46363-153">Example</span></span>

<span data-ttu-id="46363-154">**Definir o valor de um controle usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="46363-154">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="46363-155">A macro a seguir abre o formulário Adicionar produtos com um botão no formulário Suppliers.</span><span class="sxs-lookup"><span data-stu-id="46363-155">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="46363-156">Ela mostra o uso do **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **GoToControl** ações.</span><span class="sxs-lookup"><span data-stu-id="46363-156">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="46363-157">A ação **DefinirValor** define o controle de SupplierID no formulário produtos como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="46363-157">The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="46363-158">A ação **GoToControl** , em seguida, move o foco para o campo CategoryID, onde você pode começar a inserir dados para o novo produto.</span><span class="sxs-lookup"><span data-stu-id="46363-158">The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="46363-159">Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="46363-159">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46363-160">Ação</span><span class="sxs-lookup"><span data-stu-id="46363-160">Action</span></span></p></th>
<th><p><span data-ttu-id="46363-161">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="46363-161">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="46363-162">Comentário</span><span class="sxs-lookup"><span data-stu-id="46363-162">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46363-163"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="46363-163"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-164"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="46363-164"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-165">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="46363-165">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46363-166"><strong>FecharJanela</strong></span><span class="sxs-lookup"><span data-stu-id="46363-166"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-167"><strong>Tipo de objeto</strong>: <strong>Nome FormObject</strong>: lista de produto para <strong>Salvar</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="46363-167"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-168">Feche o formulário de lista de produtos.</span><span class="sxs-lookup"><span data-stu-id="46363-168">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46363-169"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="46363-169"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-170"><strong>Nome do formulário</strong>: produtos <strong>modo de exibição</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="46363-170"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-171">Abra o formulário Products.</span><span class="sxs-lookup"><span data-stu-id="46363-171">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46363-172"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="46363-172"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-173"><strong>Item</strong>: [formulários]! [Produtos]! [SupplierID] <strong>Expressão</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="46363-173"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="46363-174">Defina o controle de SupplierID como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="46363-174">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46363-175"><strong>IrParaControle</strong></span><span class="sxs-lookup"><span data-stu-id="46363-175"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="46363-176"><strong>Nome do controle</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="46363-176"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="46363-177">Vá para o controle CategoryID.</span><span class="sxs-lookup"><span data-stu-id="46363-177">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

