---
title: Ação de macro eco (referência do banco de dados do Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293620"
---
# <a name="echo-macro-action"></a><span data-ttu-id="c3901-102">Ação da macro Eco</span><span class="sxs-lookup"><span data-stu-id="c3901-102">Echo macro action</span></span>

<span data-ttu-id="c3901-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3901-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3901-104">Você pode usar a ação **eco** para especificar se o eco está ativado.</span><span class="sxs-lookup"><span data-stu-id="c3901-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="c3901-105">Por exemplo, você pode usar essa ação para ocultar ou mostrar os resultados de uma macro durante a execução.</span><span class="sxs-lookup"><span data-stu-id="c3901-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="c3901-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="c3901-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="c3901-107">This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="c3901-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="c3901-108">A ação **eco** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c3901-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3901-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="c3901-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c3901-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3901-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3901-111"><strong>Eco ativado</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-112">Clique em <strong>Sim</strong> (ativar eco) ou em <strong>não</strong> (desativar o eco) na caixa <strong>eco ativado</strong> na seção <strong>argumentos da ação</strong> do painel Construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="c3901-112">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="c3901-113">O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3901-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3901-114"><strong>Texto da Barra de Status</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-115">O texto a ser exibido na barra de status quando o eco está desativado.</span><span class="sxs-lookup"><span data-stu-id="c3901-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="c3901-116">Por exemplo, quando o eco está desativado, a barra de status pode &quot;exibir a macro está sendo executada.&quot;</span><span class="sxs-lookup"><span data-stu-id="c3901-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c3901-117">Quando uma macro é executada, a atualização de tela freqüentemente mostra informações não essenciais para o funcionamento da macro.</span><span class="sxs-lookup"><span data-stu-id="c3901-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="c3901-118">Quando você define o argumento **Echo on** como **não**, a macro é executada sem Atualizar a tela.</span><span class="sxs-lookup"><span data-stu-id="c3901-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="c3901-119">Quando a macro é concluída, o Access automaticamente ativa novamente o eco e redesenha a janela.</span><span class="sxs-lookup"><span data-stu-id="c3901-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="c3901-120">A \*\*\*\* configuração no para o argumento **Echo on** não afeta a funcionalidade da macro ou seus resultados.</span><span class="sxs-lookup"><span data-stu-id="c3901-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="c3901-121">A ação **eco** não suprime a exibição de caixas de diálogo modais, como mensagens de erro ou formulários pop-up, como folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3901-121">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="c3901-122">Você pode usar caixas de diálogo e formulários pop-up para coletar ou exibir informações, mesmo se o eco estiver desativado.</span><span class="sxs-lookup"><span data-stu-id="c3901-122">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="c3901-123">Para suprimir todas as caixas de diálogo ou mensagens de erro, exceto caixas de mensagem de erro e caixas de diálogo que exigem que o usuário insira informações, use a ação **DefinirAvisos** .</span><span class="sxs-lookup"><span data-stu-id="c3901-123">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="c3901-124">Você pode executar a ação **eco** mais de uma vez em uma macro.</span><span class="sxs-lookup"><span data-stu-id="c3901-124">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="c3901-125">Isso permite que você altere o texto da barra de status enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="c3901-125">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="c3901-126">Se você desativar o eco, poderá usar a ação **exibirponteirodeampulheta** para alterar o ponteiro do mouse para um ícone de ampulheta (ou qualquer ícone de ponteiro de mouse que você tenha definido para "ocupado") para fornecer uma indicação visual de que a macro está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="c3901-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="c3901-127">Para executar a ação **eco** em um módulo do VBA (Visual Basic for Applications), use o método **Echo** do objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="c3901-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="c3901-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c3901-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="c3901-129">Definir o valor de um controle usando uma macro</span><span class="sxs-lookup"><span data-stu-id="c3901-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="c3901-130">A macro a seguir abre o formulário Adicionar produtos a partir de um botão no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="c3901-130">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="c3901-131">Ela mostra o uso das ações **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **IrParaControle** .</span><span class="sxs-lookup"><span data-stu-id="c3901-131">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="c3901-132">A ação **DefinirValor** define o controle de ID do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="c3901-132">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="c3901-133">A ação **IrParaControle** move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto.</span><span class="sxs-lookup"><span data-stu-id="c3901-133">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="c3901-134">Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="c3901-134">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3901-135">Ação</span><span class="sxs-lookup"><span data-stu-id="c3901-135">Action</span></span></p></th>
<th><p><span data-ttu-id="c3901-136">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="c3901-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="c3901-137">Comentário</span><span class="sxs-lookup"><span data-stu-id="c3901-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3901-138"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-139"><strong>Echo ativado</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-140">Interrompa a atualização da tela enquanto a macro estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="c3901-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3901-141"><strong>FecharJanela</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-142"><strong>Tipo de objeto</strong>: <strong>nome</strong>do formObject: <strong>salvamento</strong>da lista de produtos: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-143">Feche o formulário lista de produtos.</span><span class="sxs-lookup"><span data-stu-id="c3901-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3901-144"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-145"><strong>Nome do formulário</strong>: modo de <strong>exibição</strong>de produtos: <strong>modo FormData</strong>: <strong>modo AddWindow</strong>: <strong>normal</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-146">Abra o formulário produtos.</span><span class="sxs-lookup"><span data-stu-id="c3901-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3901-147"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-148"><strong>Item</strong>: [formulários]! [Produtos]! [CódigoDoFornecedor] <strong>Expressão</strong>: CódigoDoFornecedor</span><span class="sxs-lookup"><span data-stu-id="c3901-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="c3901-149">Defina o controle de ID do fornecedor como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="c3901-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3901-150"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-151"><strong>Nome do controle</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="c3901-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="c3901-152">Vá para o controle de ID de categoria.</span><span class="sxs-lookup"><span data-stu-id="c3901-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="c3901-153">Sincronizar formulários usando uma macro</span><span class="sxs-lookup"><span data-stu-id="c3901-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="c3901-154">A macro a seguir abre o formulário lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="c3901-154">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="c3901-155">Ela mostra o uso das ações **eco**, **MessageBox**, **IrParaControle**, **PararMacro**, **AbrirFormulário**e **moveredimensionarjanela** .</span><span class="sxs-lookup"><span data-stu-id="c3901-155">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="c3901-156">Também mostra o uso de uma expressão condicional com as ações **MessageBox**, **IrParaControle**e **PararMacro** .</span><span class="sxs-lookup"><span data-stu-id="c3901-156">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="c3901-157">Essa macro deve ser anexada ao botão reVisar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="c3901-157">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3901-158">Condição</span><span class="sxs-lookup"><span data-stu-id="c3901-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="c3901-159">Ação</span><span class="sxs-lookup"><span data-stu-id="c3901-159">Action</span></span></p></th>
<th><p><span data-ttu-id="c3901-160">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="c3901-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="c3901-161">Comentário</span><span class="sxs-lookup"><span data-stu-id="c3901-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="c3901-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-163"><strong>Echo ativado</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-164">Interrompa a atualização da tela enquanto a macro estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="c3901-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3901-165">Énulo ([código do fornecedor])</span><span class="sxs-lookup"><span data-stu-id="c3901-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="c3901-166"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-167"><strong>Mensagem</strong>: mova para o registro de fornecedor cujos produtos você deseja ver e, em seguida, clique no botão revisar produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="c3901-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="c3901-168"><strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecionar um fornecedor</span><span class="sxs-lookup"><span data-stu-id="c3901-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="c3901-169">Se não houver um fornecedor atual no formulário fornecedores, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3901-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3901-170">...</span><span class="sxs-lookup"><span data-stu-id="c3901-170"></span></span></p></td>
<td><p><span data-ttu-id="c3901-171"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-172"><strong>Nome do controle</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="c3901-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="c3901-173">Mover o foco para o controle CompanyName.</span><span class="sxs-lookup"><span data-stu-id="c3901-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3901-174">...</span><span class="sxs-lookup"><span data-stu-id="c3901-174"></span></span></p></td>
<td><p><span data-ttu-id="c3901-175"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c3901-176">Interrompa a macro.</span><span class="sxs-lookup"><span data-stu-id="c3901-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="c3901-177"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-178"><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>de lista de produtos: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [CódigoDoFornecedor ID] = [formulários]! [Fornecedores]! [CódigoDoFornecedor] <strong>Modo de dados</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>normal</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-179">Abra o formulário lista de produtos e mostre os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="c3901-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="c3901-180"><strong>Moveredimensionarjanela</strong></span><span class="sxs-lookup"><span data-stu-id="c3901-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="c3901-181"><strong>direita</strong>: 0,7799&quot; <strong>baixo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="c3901-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="c3901-182">Posicione o formulário lista de produtos no canto inferior direito do formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="c3901-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

