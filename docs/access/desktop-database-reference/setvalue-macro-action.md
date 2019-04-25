---
title: Ação da macro SetValue
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306815"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="8d5f7-102">Ação da macro SetValue</span><span class="sxs-lookup"><span data-stu-id="8d5f7-102">SetValue macro action</span></span>

<span data-ttu-id="8d5f7-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d5f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d5f7-104">Você pode usar a ação **SetValue** para definir o valor de um campo do Microsoft Access, o controle ou a propriedade em um formulário, uma folha de dados do formulário ou um relatório.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>

> [!NOTE]
> - <span data-ttu-id="8d5f7-105">Não é possível usar uma ação **SetValue** para definir o valor de uma propriedade do Access que retorna um objeto.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-105">You cannot use the **SetValue** action to set the value of an Access property that returns an object.</span></span>
> - <span data-ttu-id="8d5f7-106">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="8d5f7-107">Setting</span><span class="sxs-lookup"><span data-stu-id="8d5f7-107">Setting</span></span>

<span data-ttu-id="8d5f7-108">A ação **SetValue** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-108">The **SearchForRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d5f7-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="8d5f7-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8d5f7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d5f7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d5f7-111"><strong>Item</strong></span><span class="sxs-lookup"><span data-stu-id="8d5f7-111"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-112">O nome do campo, controle ou propriedades cujo valor você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-112">The name of the field, control, or property whose value you want to set.</span></span> <span data-ttu-id="8d5f7-113">Insira o nome de campo, controle ou propriedades na caixa <strong>Item</strong> na seção <strong>Argumentos da Ação</strong> no painel do Construtor de Macros.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-113">Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="8d5f7-114">Você deve usar a sintaxe completa para fazer referência a esse item, como <em>controlname</em> (para um controle no formulário ou relatório de onde o macro foi chamado) ou <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-114">You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>.</span></span> <span data-ttu-id="8d5f7-115">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-115">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d5f7-116"><strong>Expressão</strong>.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-116"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-117">A expressão Access usa para definir o valor para esse item.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-117">The expression Access uses to set the value for this item.</span></span> <span data-ttu-id="8d5f7-118">Você sempre deve usar a sintaxe completa para referir-se a quaisquer objetos na expressão.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-118">You must always use the full syntax to refer to any objects in the expression.</span></span> <span data-ttu-id="8d5f7-119">Por exemplo, para aumentar o valor em um controle de Salário em um formulário de Funcionários em 10%, use 1.1Forms!Employees!Salary\*1.1.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-119">For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1.</span></span> <span data-ttu-id="8d5f7-120">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-120">This is a required argument.</span></span></p><p><span data-ttu-id="8d5f7-121"><strong>OBSERVAÇÃO</strong>: Você não deve usar um sinal de igual (=) antes da expressão nesse argumento.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-121"><strong>NOTE</strong>: You shouldn't use an equal sign (=) before the expression in this argument.</span></span> <span data-ttu-id="8d5f7-122">Nesse caso, o Access avalia a expressão e usa esse valor como a expressão nesse argumento.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-122">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="8d5f7-123">Isso pode produzir resultados inesperados se a expressão for uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-123">This can produce unexpected results if the expression is a string.</span></span></p>
<p><span data-ttu-id="8d5f7-124">Por exemplo, se você digitar <strong>=&quot;String1&quot;</strong> para esse argumento, o Access primeiro avalia a expressão como String1.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-124">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="8d5f7-125">Em seguida, ele usa a String1 como a expressão nesse argumento, esperando encontrar um controle ou propriedade denominada String1 no formulário ou relatório que chamou o macro.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-125">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8d5f7-126">Em um banco de dados do Access (.mdb ou .accdb), clique no botão **Build** para usar o Construtor de Expressões para criar uma expressão para qualquer um desses argumentos.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-126">In an Access database (.mdb or .accdb), click the **Build** button to use the Expression Builder to select a function for this argument.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d5f7-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d5f7-127">Remarks</span></span>

<span data-ttu-id="8d5f7-128">Você pode usar essa ação para definir um valor para um campo ou controle em um formulário, uma folha de dados do formulário ou um relatório.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-128">You can use this action to set a value for a field or control on a form, a form datasheet, or a report.</span></span> <span data-ttu-id="8d5f7-129">Você também pode definir o valor de quase todas as propriedades de controle, do formulário e do relatório em qualquer modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-129">You can also set the value for almost all control, form, and report properties in any view.</span></span> <span data-ttu-id="8d5f7-130">Para saber se uma propriedade em particular pode ser definida usando um macro e em quais modos de exibição podem ser definidas, consulte o tópico de Ajuda para essa propriedade no Editor do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-130">To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="8d5f7-131">Você também pode definir o valor para um campo em uma tabela subjacente, mesmo que a forma não contenha um controle associado ao campo.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-131">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="8d5f7-132">Usa a sintaxe **Forms**\!*formname*\!*fieldname* na caixa **Item** para definir o valor para tal campo.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-132">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="8d5f7-133">Você também pode referir um campo na tabela subjacente do relatório usando a sintaxe **Reports**\!*reportname*\!*fieldname*, mas deve haver um controle no relatório associado a esse campo ou o campo deve ser referenciado em um controle calculado no relatório.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-133">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="8d5f7-134">Se você definir o valor do controle no formulário, a ação **SetValue** não dispara regras de validação de nível de formulário de controle, mas aciona regras de validação de nível de tabela do campo subjacente se o controle for um controle associado.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-134">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control.</span></span> <span data-ttu-id="8d5f7-135">A ação **SetValue** também aciona um recálculo, mas o recálculo pode não ocorrer imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-135">The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately.</span></span> <span data-ttu-id="8d5f7-136">Para acionar a repintura imediata e forçar o recálculo até a conclusão, use a ação **RepaintObject**.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-136">To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action.</span></span> <span data-ttu-id="8d5f7-137">O valor definido em um controle usando a ação **SetValue** também não é afetado por uma máscara de entrada definida na propriedade **InputMask** do campo subjacente ou do controle.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-137">The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="8d5f7-138">Para alterar o valor de um controle, você pode usar a ação **SetValue** em um macro especificado pela propriedade do evento **AfterUpdate** do controle.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-138">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property.</span></span> <span data-ttu-id="8d5f7-139">No entanto, é possível usar a ação **SetValue** em um macro especificado pela propriedade do evento **BeforeUpdate** do controle para alterar o valor do controle (embora você possa usar a ação **SetValue** para alterar o valor dos outros controles).</span><span class="sxs-lookup"><span data-stu-id="8d5f7-139">However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls).</span></span> <span data-ttu-id="8d5f7-140">Você também pode usar a ação **SetValue** em um macro especificado pela propriedade **BeforeUpdate** ou **AfterUpdate** de um formulário para alterar o valor de todos os controles do atual registro.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-140">You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>

> [!NOTE]
> <span data-ttu-id="8d5f7-141">Não é possível usar a ação **SetValue** para definir o valor dos controles a seguir:</span><span class="sxs-lookup"><span data-stu-id="8d5f7-141">You can't use the **SetValue** action to set the value of the following controls:</span></span>
> - <span data-ttu-id="8d5f7-142">Controles associados e os controles calculados em relatórios.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-142">Bound controls and calculated controls on reports.</span></span>
> - <span data-ttu-id="8d5f7-143">Controles calculados em formulários.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-143">Calculated controls on forms.</span></span>

> [!TIP]
> <span data-ttu-id="8d5f7-144">Você pode usar a ação **SetValue** para mostrar ou ocultar um formulário no modo de exibição Formulário.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-144">You can use the **SetValue** action to hide or show a form in Form view.</span></span> <span data-ttu-id="8d5f7-145">Insira **Forms**!*formname\*\*\*.Visible*\* na caixa **Item** box, e **Não** ou **Sim** na caixa **Expressão**.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-145">Enter **Forms**!*formname\*\*\*.Visible*\* in the **Item** box, and **No** or **Yes** in the **Expression** box.</span></span> <span data-ttu-id="8d5f7-146">Definir uma propriedade modal **Visível** do formulário para **Não** oculta o formulário e o torna sem restrição.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-146">Setting a modal form's **Visible** property to **No** hides the form and makes it modeless.</span></span> <span data-ttu-id="8d5f7-147">Definir a propriedade para **Sim** exibe o formulário e o torna restrito novamente.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-147">Setting the property to **Yes** displays the form and makes it modal again.</span></span>

<span data-ttu-id="8d5f7-148">Alterar o valor de ou adicionar novos dados em um controle usando a ação**SetValue** em um macro não dispara, eventos como **BeforeUpdate**, **BeforeInsert**, ou **Change** que ocorrem quando você altera ou insere dados em um desses controles na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-148">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface.</span></span> <span data-ttu-id="8d5f7-149">Esses eventos também não ocorrerem se você definir o valor do controle usando um módulo do Visual Basic for Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="8d5f7-149">These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="8d5f7-150">Essa ação não está disponível em um módulo do VBA.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-150">This action isn't available in a VBA module.</span></span> <span data-ttu-id="8d5f7-151">Defina o valor diretamente no VBA.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-151">Set the value directly in Visual Basic.</span></span>

## <a name="example"></a><span data-ttu-id="8d5f7-152">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8d5f7-152">Example</span></span>

<span data-ttu-id="8d5f7-153">**Definir o valor de um controle usando um macro**</span><span class="sxs-lookup"><span data-stu-id="8d5f7-153">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="8d5f7-154">O macro a seguir abre o formulário Adicionar Produtos de um botão no formulário de Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-154">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="8d5f7-155">Mostra o uso das ações **Echo**, **CloseWindow**, **OpenForm**, **SetValue** e **GoToControl** actions.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-155">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="8d5f7-156">A ação **SetValue** define o controle SupplierID no formulário de Produtos dos fornecedores atuais no formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-156">The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="8d5f7-157">A ação **GoToControl** move o foco para o campo CategoryID, onde você pode começar a inserir dados do novo produto.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-157">The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="8d5f7-158">Esse macro deve estar anexado ao botão Adicionar Produtos no formulário de Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-158">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d5f7-159">Ação</span><span class="sxs-lookup"><span data-stu-id="8d5f7-159">Action</span></span></p></th>
<th><p><span data-ttu-id="8d5f7-160">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="8d5f7-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="8d5f7-161">Comentário</span><span class="sxs-lookup"><span data-stu-id="8d5f7-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d5f7-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="8d5f7-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-163"><strong>Echo On</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="8d5f7-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-164">Interrompe a atualização de tela quando macro é executado.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d5f7-165"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="8d5f7-165"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-166"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="8d5f7-166"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-167">Fecha o Formulário de Lista de Produtos.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-167">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d5f7-168"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="8d5f7-168"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-169"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="8d5f7-169"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-170">Abre o formulário de produtos.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-170">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d5f7-171"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="8d5f7-171"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-172"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="8d5f7-172"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="8d5f7-173">Define o controle SupplierID para o fornecedor atual no formulário de Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-173">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d5f7-174"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="8d5f7-174"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="8d5f7-175"><strong>Control Name</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="8d5f7-175"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="8d5f7-176">Vai para o controle CategoryID.</span><span class="sxs-lookup"><span data-stu-id="8d5f7-176">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

