---
title: Ação da macro CaixaDeMensagem
TOCTitle: MessageBox macro action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1175e3903e54fd3420be43dfd9e3652d9990468b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722925"
---
# <a name="messagebox-macro-action"></a><span data-ttu-id="82526-102">Ação da macro CaixaDeMensagem</span><span class="sxs-lookup"><span data-stu-id="82526-102">MessageBox macro action</span></span>

<span data-ttu-id="82526-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="82526-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82526-104">Você pode usar a ação **MessageBox** para exibir uma caixa de mensagem contendo um aviso ou uma mensagem informativa.</span><span class="sxs-lookup"><span data-stu-id="82526-104">You can use the **MessageBox** action to display a message box containing a warning or an informational message.</span></span> <span data-ttu-id="82526-105">Por exemplo, você pode usar a ação **MessageBox** com macros de validação.</span><span class="sxs-lookup"><span data-stu-id="82526-105">For example, you can use the **MessageBox** action with validation macros.</span></span> <span data-ttu-id="82526-106">Quando um controle ou registro falha uma condição de validação na macro, uma caixa de mensagem pode exibir uma mensagem de erro e forneça instruções sobre o tipo de dados que devem ser inseridos.</span><span class="sxs-lookup"><span data-stu-id="82526-106">When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span>

## <a name="setting"></a><span data-ttu-id="82526-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="82526-107">Setting</span></span>

<span data-ttu-id="82526-108">A ação de **MessageBox** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="82526-108">The **MessageBox** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82526-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="82526-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="82526-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="82526-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82526-111"><strong>Message</strong></span><span class="sxs-lookup"><span data-stu-id="82526-111"><strong>Message</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-112">O texto na caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="82526-112">The text in the message box.</span></span> <span data-ttu-id="82526-113">Insira o texto da mensagem na caixa de <strong>mensagem</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="82526-113">Enter the message text in the <strong>Message</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="82526-114">Você pode digitar até 255 caracteres ou inserir uma expressão (precedida por um sinal de igualdade).</span><span class="sxs-lookup"><span data-stu-id="82526-114">You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82526-115"><strong>Beep</strong></span><span class="sxs-lookup"><span data-stu-id="82526-115"><strong>Beep</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-116">Especifica se o alto-falante do seu computador emitirá um aviso sonoro quando a mensagem é exibida.</span><span class="sxs-lookup"><span data-stu-id="82526-116">Specifies whether your computer's speaker sounds a beep tone when the message displays.</span></span> <span data-ttu-id="82526-117">Clique em <strong>Sim</strong> (som o aviso sonoro) ou <strong>não</strong> (não SOA o aviso sonoro).</span><span class="sxs-lookup"><span data-stu-id="82526-117">Click <strong>Yes</strong> (sound the beep tone) or <strong>No</strong> (don't sound the beep tone).</span></span> <span data-ttu-id="82526-118">O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="82526-118">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82526-119"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="82526-119"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-120">O tipo de caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="82526-120">The type of message box.</span></span> <span data-ttu-id="82526-121">Cada tipo tem um ícone diferente.</span><span class="sxs-lookup"><span data-stu-id="82526-121">Each type has a different icon.</span></span> <span data-ttu-id="82526-122">Clique em <strong>Nenhum</strong>, <strong>crítico</strong>, <strong>Aviso?</strong>, <strong>Aviso!</strong>, ou <strong>informações</strong>.</span><span class="sxs-lookup"><span data-stu-id="82526-122">Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>.</span></span> <span data-ttu-id="82526-123">O padrão é <strong>None</strong>.</span><span class="sxs-lookup"><span data-stu-id="82526-123">The default is <strong>None</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82526-124"><strong>Title</strong></span><span class="sxs-lookup"><span data-stu-id="82526-124"><strong>Title</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-125">O texto exibido na barra de título da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="82526-125">The text displayed in the message box title bar.</span></span> <span data-ttu-id="82526-126">Por exemplo, você pode ter a exibição da barra de título &quot;validação de ID de cliente&quot;.</span><span class="sxs-lookup"><span data-stu-id="82526-126">For example, you can have the title bar display &quot;Customer ID Validation&quot;.</span></span> <span data-ttu-id="82526-127">Se você deixar este argumento em branco, &quot;Microsoft Access&quot; é exibida.</span><span class="sxs-lookup"><span data-stu-id="82526-127">If you leave this argument blank, &quot;Microsoft Access&quot; is displayed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="82526-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="82526-128">Remarks</span></span>

<span data-ttu-id="82526-129">Você pode usar a ação **MessageBox** para criar uma mensagem de erro formatada semelhante às mensagens de erro internas exibidas pelo Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="82526-129">You can use the **MessageBox** action to create a formatted error message similar to built-in error messages displayed by Microsoft Access.</span></span> <span data-ttu-id="82526-130">A ação **MessageBox** permite fornecer uma mensagem em três seções para o argumento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="82526-130">The **MessageBox** action permits you to supply a message in three sections for the Message argument.</span></span> <span data-ttu-id="82526-131">Separa as seções com o "@" caractere.</span><span class="sxs-lookup"><span data-stu-id="82526-131">You separate the sections with the "@" character.</span></span>

<span data-ttu-id="82526-132">O exemplo a seguir exibe uma caixa de mensagem formatada com uma mensagem dividida em seções.</span><span class="sxs-lookup"><span data-stu-id="82526-132">The following example displays a formatted message box with a sectioned message.</span></span> <span data-ttu-id="82526-133">A primeira seção do texto da mensagem é exibida como um cabeçalho em negrito.</span><span class="sxs-lookup"><span data-stu-id="82526-133">The first section of text in the message is displayed as a bold heading.</span></span> <span data-ttu-id="82526-134">A segunda seção é exibida como texto sem formatação abaixo do título.</span><span class="sxs-lookup"><span data-stu-id="82526-134">The second section is displayed as plain text beneath that heading.</span></span> <span data-ttu-id="82526-135">A terceira seção é exibida como texto simples abaixo da segunda seção, com uma linha em branco entre elas.</span><span class="sxs-lookup"><span data-stu-id="82526-135">The third section is displayed as plain text beneath the second section, with a blank line between them.</span></span>

<span data-ttu-id="82526-136">Digite a cadeia de caracteres a seguir no argumento **mensagem** :</span><span class="sxs-lookup"><span data-stu-id="82526-136">Type the following string in the **Message** argument:</span></span>

<span data-ttu-id="82526-137">**Botão errado\!@This botão não Work.@Try outro.**</span><span class="sxs-lookup"><span data-stu-id="82526-137">**Wrong button\!@This button doesn't work.@Try another.**</span></span>

<span data-ttu-id="82526-138">Você não pode executar a ação de **MessageBox** em um módulo Visual Basic for Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="82526-138">You can't run the **MessageBox** action in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="82526-139">Use a função **MsgBox** .</span><span class="sxs-lookup"><span data-stu-id="82526-139">Use the **MsgBox** function instead.</span></span>

## <a name="examples"></a><span data-ttu-id="82526-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82526-140">Examples</span></span>

<span data-ttu-id="82526-141">**Sincronizar formulários usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="82526-141">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="82526-142">A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="82526-142">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="82526-143">Ela mostra o uso do **eco**, **MessageBox**, **GoToControl**, **PararMacro**, **AbrirFormulário**e **Moveredimensionarjanela** ações.</span><span class="sxs-lookup"><span data-stu-id="82526-143">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="82526-144">Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl**e **PararMacro** .</span><span class="sxs-lookup"><span data-stu-id="82526-144">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="82526-145">Essa macro deve ser anexada ao botão Revisar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="82526-145">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82526-146">Condição</span><span class="sxs-lookup"><span data-stu-id="82526-146">Condition</span></span></p></th>
<th><p><span data-ttu-id="82526-147">Ação</span><span class="sxs-lookup"><span data-stu-id="82526-147">Action</span></span></p></th>
<th><p><span data-ttu-id="82526-148">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="82526-148">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="82526-149">Comentário</span><span class="sxs-lookup"><span data-stu-id="82526-149">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="82526-150"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="82526-150"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-151"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="82526-151"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-152">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="82526-152">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82526-153">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="82526-153">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="82526-154"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="82526-154"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-155"><strong>Mensagem</strong>: mover para o registro do fornecedor cujos produtos você deseja ver, em seguida, clique no botão Revisar produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="82526-155"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="82526-156"><strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecione um fornecedor</span><span class="sxs-lookup"><span data-stu-id="82526-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="82526-157">Se não houver nenhum fornecedor atual no formulário fornecedores, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="82526-157">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82526-158">...</span><span class="sxs-lookup"><span data-stu-id="82526-158"></span></span></p></td>
<td><p><span data-ttu-id="82526-159"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="82526-159"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-160"><strong>Nome do controle</strong>: NomeDaEmpresa</span><span class="sxs-lookup"><span data-stu-id="82526-160"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="82526-161">Mova o foco para o controle NomeDaEmpresa.</span><span class="sxs-lookup"><span data-stu-id="82526-161">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82526-162">...</span><span class="sxs-lookup"><span data-stu-id="82526-162"></span></span></p></td>
<td><p><span data-ttu-id="82526-163"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="82526-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="82526-164">Interrompa a macro.</span><span class="sxs-lookup"><span data-stu-id="82526-164">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="82526-165"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="82526-165"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-166"><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>da lista de produto: <strong>DatasheetFilter nome</strong>: <strong>condição onde</strong>: [SupplierID] = [formulários]! Fornecedores! [SupplierID] <strong>Modo de dados</strong>: <strong>Modo de OnlyWindow de leitura</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="82526-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-167">Abra o formulário de lista de produtos e mostram os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="82526-167">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="82526-168"><strong>Moveredimensionarjanela</strong></span><span class="sxs-lookup"><span data-stu-id="82526-168"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-169"><strong>Direita</strong>: 0.7799&quot; <strong>para baixo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="82526-169"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="82526-170">Posiciona o formulário de lista de produtos no canto inferior direito do formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="82526-170">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="82526-171">**Validar dados usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="82526-171">**Validate data by using a macro**</span></span>

<span data-ttu-id="82526-172">A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="82526-172">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="82526-173">Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**.</span><span class="sxs-lookup"><span data-stu-id="82526-173">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="82526-174">Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário.</span><span class="sxs-lookup"><span data-stu-id="82526-174">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="82526-175">Se o código postal não estiver no formato correto para o país/região, a macro exibe uma caixa de mensagem e cancela o registro é salvo.</span><span class="sxs-lookup"><span data-stu-id="82526-175">If the postal code isn't in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="82526-176">Ele então retorna você ao controle PostalCode, onde é possível corrigir o erro.</span><span class="sxs-lookup"><span data-stu-id="82526-176">It then returns you to the PostalCode control, where you can correct the error.</span></span> <span data-ttu-id="82526-177">Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="82526-177">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82526-178">Condição</span><span class="sxs-lookup"><span data-stu-id="82526-178">Condition</span></span></p></th>
<th><p><span data-ttu-id="82526-179">Ação</span><span class="sxs-lookup"><span data-stu-id="82526-179">Action</span></span></p></th>
<th><p><span data-ttu-id="82526-180">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="82526-180">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="82526-181">Comentário</span><span class="sxs-lookup"><span data-stu-id="82526-181">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82526-182">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="82526-182">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="82526-183"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="82526-183"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="82526-184">Se CountryRegion for <strong>Nulo</strong>, o código postal não pode ser validado.</span><span class="sxs-lookup"><span data-stu-id="82526-184">If CountryRegion is <strong>Null</strong>, the postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82526-185">[Paísregião] No (&quot;França&quot;,&quot;Itália&quot;,&quot;Espanha&quot;) e Len([PostalCode]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="82526-185">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([PostalCode]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="82526-186"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="82526-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-187"><strong>Mensagem</strong>: O código postal precisa ter 5 caracteres.</span><span class="sxs-lookup"><span data-stu-id="82526-187"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="82526-188"><strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de CEP</span><span class="sxs-lookup"><span data-stu-id="82526-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="82526-189">Se o código postal não tiver 5 caracteres, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="82526-189">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82526-190">...</span><span class="sxs-lookup"><span data-stu-id="82526-190"></span></span></p></td>
<td><p><span data-ttu-id="82526-191"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="82526-191"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="82526-192">Cancele o evento.</span><span class="sxs-lookup"><span data-stu-id="82526-192">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="82526-193"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="82526-193"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-194"><strong>Nome do controle</strong>: CEP</span><span class="sxs-lookup"><span data-stu-id="82526-194"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82526-195">[Paísregião] No (&quot;Austrália&quot;,&quot;Cingapura&quot;) e Len([PostalCode]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="82526-195">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([PostalCode]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="82526-196"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="82526-196"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-197"><strong>Mensagem</strong>: O código postal precisa ter 4 caracteres.</span><span class="sxs-lookup"><span data-stu-id="82526-197"><strong>Message</strong>: The postal code must be 4 characters.</span></span> <span data-ttu-id="82526-198"><strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de CEP</span><span class="sxs-lookup"><span data-stu-id="82526-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="82526-199">Se o código postal não tiver 4 caracteres, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="82526-199">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82526-200">...</span><span class="sxs-lookup"><span data-stu-id="82526-200"></span></span></p></td>
<td><p><span data-ttu-id="82526-201"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="82526-201"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="82526-202">Cancele o evento.</span><span class="sxs-lookup"><span data-stu-id="82526-202">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="82526-203"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="82526-203"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-204"><strong>Nome do controle</strong>: CEP</span><span class="sxs-lookup"><span data-stu-id="82526-204"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82526-205">([Paísregião] = &quot;Canadá&quot;) E ([CEP] não igual a&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="82526-205">([CountryRegion] = &quot;Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="82526-206"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="82526-206"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="82526-207"><strong>Mensagem</strong>: O código postal não é válido.</span><span class="sxs-lookup"><span data-stu-id="82526-207"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="82526-208">Exemplo de código canadense: H1J 1C3 <strong>alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código Postal</span><span class="sxs-lookup"><span data-stu-id="82526-208">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="82526-p115">Se o código postal não estiver correto para Canadá, exiba uma mensagem. (Exemplo de código de Canadá: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="82526-p115">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82526-211">...</span><span class="sxs-lookup"><span data-stu-id="82526-211"></span></span></p></td>
<td><p><span data-ttu-id="82526-212"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="82526-212"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="82526-213">Cancele o evento.</span><span class="sxs-lookup"><span data-stu-id="82526-213">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

