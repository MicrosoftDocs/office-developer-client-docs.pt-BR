---
title: Ação de Macro GoToControl
TOCTitle: GoToControl Macro Action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d068f6e0087d93d4a7dec3c5a7b2ed0f11c36be7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874857"
---
# <a name="gotocontrol-macro-action"></a><span data-ttu-id="3b51f-102">Ação de Macro GoToControl</span><span class="sxs-lookup"><span data-stu-id="3b51f-102">GoToControl Macro Action</span></span>


<span data-ttu-id="3b51f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b51f-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="3b51f-104">Você pode usar a ação **GoToControl** para mover o foco para o campo ou controle especificado no registro atual do formulário aberto, folha de dados de formulário, folha de dados da tabela ou consulta a folha de dados.</span><span class="sxs-lookup"><span data-stu-id="3b51f-104">You can use the **GoToControl** action to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet.</span></span> <span data-ttu-id="3b51f-105">Use esta ação quando quiser que um campo ou controle específico tenha o foco.</span><span class="sxs-lookup"><span data-stu-id="3b51f-105">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="3b51f-106">Esse campo ou controle pode ser usado para comparações ou ações **EncontrarRegistro** .</span><span class="sxs-lookup"><span data-stu-id="3b51f-106">This field or control can then be used for comparisons or **FindRecord** actions.</span></span> <span data-ttu-id="3b51f-107">Você também pode usar esta ação para navegar em um formulário de acordo com certas condições.</span><span class="sxs-lookup"><span data-stu-id="3b51f-107">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="3b51f-108">Por exemplo, se o usuário inserir Não em um controle Casado de um formulário de seguro de saúde, o foco automaticamente poderá ignorar o controle Nome do cônjuge/parceiro e passar para o próximo controle.</span><span class="sxs-lookup"><span data-stu-id="3b51f-108">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>

## <a name="setting"></a><span data-ttu-id="3b51f-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="3b51f-109">Setting</span></span>


> [!NOTE]
> <P><span data-ttu-id="3b51f-110">Essa ação não está disponível para uso com páginas de acesso a dados.</span><span class="sxs-lookup"><span data-stu-id="3b51f-110">This action is not available for use with data access pages.</span></span></P>



<span data-ttu-id="3b51f-111">A ação **IrParaControle** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b51f-111">The **GoToControl** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b51f-112">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="3b51f-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3b51f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b51f-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b51f-114"><strong>Nome do Controle</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-114"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-115">O nome do campo ou do controle em que você deseja focar.</span><span class="sxs-lookup"><span data-stu-id="3b51f-115">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="3b51f-116">Insira o nome do campo ou controle na caixa <strong>Nome do controle</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="3b51f-116">Enter the field or control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="3b51f-117">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3b51f-117">This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="3b51f-118">Insira apenas o nome do campo ou controle no argumento <STRONG>Nome do controle</STRONG> , não o identificador totalmente qualificado, como formulários! Produtos! [Product ID].</span><span class="sxs-lookup"><span data-stu-id="3b51f-118">Enter only the name of the field or control in the <STRONG>Control Name</STRONG> argument, not the fully qualified identifier, such as Forms!Products![Product ID].</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3b51f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b51f-119">Remarks</span></span>

<span data-ttu-id="3b51f-120">Você não pode usar a ação **GoToControl** para mover o foco para um controle em um formulário oculto.</span><span class="sxs-lookup"><span data-stu-id="3b51f-120">You cannot use the **GoToControl** action to move the focus to a control on a hidden form.</span></span>


> [!TIP]
> <P><span data-ttu-id="3b51f-121">Você pode usar a ação <STRONG>GoToControl</STRONG> para mover para o subformulário, que é um tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="3b51f-121">You can use the <STRONG>GoToControl</STRONG> action to move to a subform, which is a type of control.</span></span> <span data-ttu-id="3b51f-122">Em seguida, você pode usar a ação <STRONG>IrParaRegistro</STRONG> para mover para um determinado registro no subformulário.</span><span class="sxs-lookup"><span data-stu-id="3b51f-122">You can then use the <STRONG>GoToRecord</STRONG> action to move to a particular record in the subform.</span></span> <span data-ttu-id="3b51f-123">Você também pode mover para um controle em um subformulário, usando a ação <STRONG>GoToControl</STRONG> para mover-se primeiro para o subformulário e, em seguida, para o controle no subformulário.</span><span class="sxs-lookup"><span data-stu-id="3b51f-123">You can also move to a control on a subform by using the <STRONG>GoToControl</STRONG> action to move first to the subform and then to the control on the subform.</span></span></P>



<span data-ttu-id="3b51f-124">Para executar a ação **GoToControl** em um módulo Visual Basic for Applications (VBA), use o método **GoToControl** do objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="3b51f-124">To run the **GoToControl** action in a Visual Basic for Applications (VBA) module, use the **GoToControl** method of the **DoCmd** object.</span></span> <span data-ttu-id="3b51f-125">Você também pode usar o método **SetFocus** para mover o foco para um controle em um formulário ou qualquer um dos seus subformulários ou para um campo em uma tabela aberta, consulta ou folha de dados do formulário.</span><span class="sxs-lookup"><span data-stu-id="3b51f-125">You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.</span></span>

## <a name="examples"></a><span data-ttu-id="3b51f-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b51f-126">Examples</span></span>

<span data-ttu-id="3b51f-127">**Definir o valor de um controle usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="3b51f-127">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="3b51f-128">A macro a seguir abre o formulário Adicionar produtos com um botão no formulário Suppliers.</span><span class="sxs-lookup"><span data-stu-id="3b51f-128">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="3b51f-129">Ela mostra o uso do **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **GoToControl** ações.</span><span class="sxs-lookup"><span data-stu-id="3b51f-129">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="3b51f-130">A ação **DefinirValor** define o controle de código do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="3b51f-130">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="3b51f-131">A ação **GoToControl** , em seguida, move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto.</span><span class="sxs-lookup"><span data-stu-id="3b51f-131">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="3b51f-132">Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="3b51f-132">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b51f-133">Ação</span><span class="sxs-lookup"><span data-stu-id="3b51f-133">Action</span></span></p></th>
<th><p><span data-ttu-id="3b51f-134">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="3b51f-134">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="3b51f-135">Comentário</span><span class="sxs-lookup"><span data-stu-id="3b51f-135">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b51f-136"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-136"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-137"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-137"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-138">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="3b51f-138">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b51f-139"><strong>FecharJanela</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-139"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-140"><strong>Tipo de objeto</strong>: <strong>Nome FormObject</strong>: lista de produto para <strong>Salvar</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-140"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-141">Fechar o formulário de lista de produtos.</span><span class="sxs-lookup"><span data-stu-id="3b51f-141">Close Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b51f-142"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-142"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-143"><strong>Nome do formulário</strong>: produtos <strong>modo de exibição</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-143"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-144">Abra o formulário Products.</span><span class="sxs-lookup"><span data-stu-id="3b51f-144">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b51f-145"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-145"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-146"><strong>Item</strong>: [formulários]! [Produtos]! [SupplierID] <strong>Expressão</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="3b51f-146"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="3b51f-147">Defina o controle de código do fornecedor como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="3b51f-147">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b51f-148"><strong>IrParaControle</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-148"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-149"><strong>Nome do controle</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="3b51f-149"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="3b51f-150">Vá para o controle de ID da categoria.</span><span class="sxs-lookup"><span data-stu-id="3b51f-150">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b51f-151">**Validar dados usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="3b51f-151">**Validate data by using a macro**</span></span>

<span data-ttu-id="3b51f-152">A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="3b51f-152">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="3b51f-153">Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**.</span><span class="sxs-lookup"><span data-stu-id="3b51f-153">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="3b51f-154">Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário.</span><span class="sxs-lookup"><span data-stu-id="3b51f-154">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="3b51f-155">Se o código postal não estiver no formato certo para o país/região, a macro exibirá uma caixa de mensagem e cancelará o salvamento do registro.</span><span class="sxs-lookup"><span data-stu-id="3b51f-155">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="3b51f-156">A macro retorna você ao controle CEP, onde é possível corrigir o erro.</span><span class="sxs-lookup"><span data-stu-id="3b51f-156">The macro then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="3b51f-157">Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="3b51f-157">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b51f-158">Condição</span><span class="sxs-lookup"><span data-stu-id="3b51f-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="3b51f-159">Ação</span><span class="sxs-lookup"><span data-stu-id="3b51f-159">Action</span></span></p></th>
<th><p><span data-ttu-id="3b51f-160">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="3b51f-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="3b51f-161">Comentário</span><span class="sxs-lookup"><span data-stu-id="3b51f-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b51f-162">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="3b51f-162">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="3b51f-163"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3b51f-164">Se CountryRegion for <strong>Nulo</strong>, o código postal não pode ser validado.</span><span class="sxs-lookup"><span data-stu-id="3b51f-164">If CountryRegion is <strong>Null</strong>, postal code cannot be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b51f-165">[Paísregião] No (&quot;França&quot;,&quot;Itália&quot;,&quot;Espanha&quot;) e Compr ([CEP]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="3b51f-165">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="3b51f-166"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-167"><strong>Mensagem</strong>: O código postal precisa ter 5 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3b51f-167"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="3b51f-168"><strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de CEP</span><span class="sxs-lookup"><span data-stu-id="3b51f-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="3b51f-169">Se o código postal não tiver 5 caracteres, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b51f-169">If the postal code is not 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b51f-170">...</span><span class="sxs-lookup"><span data-stu-id="3b51f-170"></span></span></p></td>
<td><p><span data-ttu-id="3b51f-171"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-171"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3b51f-172">Cancele o evento.</span><span class="sxs-lookup"><span data-stu-id="3b51f-172">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="3b51f-173"><strong>IrParaControle</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-173"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-174"><strong>Nome do controle</strong>: CEP</span><span class="sxs-lookup"><span data-stu-id="3b51f-174"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b51f-175">[Paísregião] No (&quot;Austrália&quot;,&quot;Cingapura&quot;) e Compr ([CEP]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="3b51f-175">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="3b51f-176"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-176"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-177">Mensagem: O código postal precisa ter 4 caracteres. 

</span><span class="sxs-lookup"><span data-stu-id="3b51f-177">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="3b51f-178"><strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de CEP</span><span class="sxs-lookup"><span data-stu-id="3b51f-178"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="3b51f-179">Se o código postal não tiver 4 caracteres, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b51f-179">If the postal code is not 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b51f-180">...</span><span class="sxs-lookup"><span data-stu-id="3b51f-180"></span></span></p></td>
<td><p><span data-ttu-id="3b51f-181"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-181"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3b51f-182">Cancele o evento.</span><span class="sxs-lookup"><span data-stu-id="3b51f-182">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="3b51f-183"><strong>IrParaControle</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-183"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-184"><strong>Nome do controle</strong>: CEP</span><span class="sxs-lookup"><span data-stu-id="3b51f-184"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b51f-185">([Paísregião] = &quot;Canadá&quot;) E ([CEP] não igual a&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="3b51f-185">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="3b51f-186"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="3b51f-187"><strong>Mensagem</strong>: O código postal não é válido.</span><span class="sxs-lookup"><span data-stu-id="3b51f-187"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="3b51f-188">Exemplo de código canadense: H1J 1C3 <strong>alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código Postal</span><span class="sxs-lookup"><span data-stu-id="3b51f-188">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="3b51f-189">Se o código postal não estiver correto para o Canadá, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b51f-189">If the postal code is not correct for Canada, display a message.</span></span> <span data-ttu-id="3b51f-190">(O exemplo de código canadense: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="3b51f-190">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b51f-191">...</span><span class="sxs-lookup"><span data-stu-id="3b51f-191"></span></span></p></td>
<td><p><span data-ttu-id="3b51f-192"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="3b51f-192"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="3b51f-193">Cancele o evento.</span><span class="sxs-lookup"><span data-stu-id="3b51f-193">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

