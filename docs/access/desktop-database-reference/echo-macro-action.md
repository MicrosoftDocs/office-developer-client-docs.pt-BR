---
title: Ação de macro de eco (referência de banco de dados da área de trabalho do Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710661"
---
# <a name="echo-macro-action"></a><span data-ttu-id="d711b-102">Ação da macro Eco</span><span class="sxs-lookup"><span data-stu-id="d711b-102">Echo macro action</span></span>

<span data-ttu-id="d711b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d711b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d711b-104">Você pode usar a ação **eco** para especificar se o eco está ativado.</span><span class="sxs-lookup"><span data-stu-id="d711b-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="d711b-105">Por exemplo, você pode usar essa ação para ocultar ou mostrar os resultados de uma macro enquanto ele é executado.</span><span class="sxs-lookup"><span data-stu-id="d711b-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="d711b-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="d711b-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="d711b-107">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="d711b-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="d711b-108">A ação **eco** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d711b-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d711b-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="d711b-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d711b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d711b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d711b-111"><strong>Eco ativo</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-112">Clique em <strong>Sim</strong> (ativar o eco) ou <strong>não</strong> (desativar o eco) na caixa <strong>Eco na</strong> seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="d711b-112">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="d711b-113">O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="d711b-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d711b-114"><strong>Texto da Barra de Status</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-115">O texto a ser exibido na barra quando o eco está desativado de status.</span><span class="sxs-lookup"><span data-stu-id="d711b-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="d711b-116">Por exemplo, quando o eco está desativado, a barra de status pode exibir &quot;a macro está sendo executada.&quot;</span><span class="sxs-lookup"><span data-stu-id="d711b-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d711b-117">Quando uma macro for executada, a atualização da tela frequentemente mostra informações que não são essenciais para o funcionamento da macro.</span><span class="sxs-lookup"><span data-stu-id="d711b-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="d711b-118">Quando você define o argumento **Echo ativo** como **não**, a macro será executada sem atualizar a tela.</span><span class="sxs-lookup"><span data-stu-id="d711b-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="d711b-119">Quando a macro é concluída, o Access automaticamente ativa eco e redesenha a janela.</span><span class="sxs-lookup"><span data-stu-id="d711b-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="d711b-120">A configuração **não** para o argumento **Eco ativo** não afeta a funcionalidade da macro ou seus resultados.</span><span class="sxs-lookup"><span data-stu-id="d711b-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="d711b-121">A ação **Echo** não suprime a exibição de caixas de diálogo modal, mensagens de erro ou formulários pop-up, como folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d711b-121">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="d711b-122">Você pode usar caixas de diálogo e formulários pop-up para coletar ou exibir informações, mesmo se o eco está desativado.</span><span class="sxs-lookup"><span data-stu-id="d711b-122">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="d711b-123">Para suprimir todas as caixas de diálogo ou de mensagem, exceto as caixas de mensagem de erro e caixas de diálogo que exigem que o usuário insira informações, use a ação **DefinirAvisos** .</span><span class="sxs-lookup"><span data-stu-id="d711b-123">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="d711b-124">Você pode executar a ação **eco** mais de uma vez em uma macro.</span><span class="sxs-lookup"><span data-stu-id="d711b-124">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="d711b-125">Isso permite que você altere o texto da barra de status enquanto a macro será executada.</span><span class="sxs-lookup"><span data-stu-id="d711b-125">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="d711b-126">Se você desativar o eco, você pode usar a ação **Exibirponteirodeampulheta** para alterar o ponteiro do mouse em um ícone de ampulheta (ou qualquer outro ícone de ponteiro do mouse definido para "Ocupado") para fornecer uma indicação visual que a macro está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="d711b-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="d711b-127">Para executar a ação **eco** em um módulo Visual Basic for Applications (VBA), use o método **Echo** do objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="d711b-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="d711b-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d711b-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="d711b-129">Definir o valor de um controle usando uma macro</span><span class="sxs-lookup"><span data-stu-id="d711b-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="d711b-130">A macro a seguir abre o formulário Adicionar produtos com um botão no formulário Suppliers.</span><span class="sxs-lookup"><span data-stu-id="d711b-130">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="d711b-131">Ela mostra o uso do **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **GoToControl** ações.</span><span class="sxs-lookup"><span data-stu-id="d711b-131">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="d711b-132">A ação **DefinirValor** define o controle de código do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="d711b-132">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="d711b-133">A ação **GoToControl** , em seguida, move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto.</span><span class="sxs-lookup"><span data-stu-id="d711b-133">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="d711b-134">Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="d711b-134">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d711b-135">Ação</span><span class="sxs-lookup"><span data-stu-id="d711b-135">Action</span></span></p></th>
<th><p><span data-ttu-id="d711b-136">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="d711b-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="d711b-137">Comentário</span><span class="sxs-lookup"><span data-stu-id="d711b-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d711b-138"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-139"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-140">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="d711b-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d711b-141"><strong>FecharJanela</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-142"><strong>Tipo de objeto</strong>: <strong>Nome FormObject</strong>: lista de produto para <strong>Salvar</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-143">Feche o formulário de lista de produtos.</span><span class="sxs-lookup"><span data-stu-id="d711b-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d711b-144"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-145"><strong>Nome do formulário</strong>: produtos <strong>modo de exibição</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-146">Abra o formulário Products.</span><span class="sxs-lookup"><span data-stu-id="d711b-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d711b-147"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-148"><strong>Item</strong>: [formulários]! [Produtos]! [SupplierID] <strong>Expressão</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="d711b-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="d711b-149">Defina o controle de código do fornecedor como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="d711b-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d711b-150"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-151"><strong>Nome do controle</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="d711b-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="d711b-152">Vá para o controle de ID da categoria.</span><span class="sxs-lookup"><span data-stu-id="d711b-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="d711b-153">Sincronizar formulários usando uma macro</span><span class="sxs-lookup"><span data-stu-id="d711b-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="d711b-154">A macro a seguir abre o formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="d711b-154">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="d711b-155">Ela mostra o uso do **eco**, **MessageBox**, **GoToControl**, **PararMacro**, **AbrirFormulário**e **Moveredimensionarjanela** ações.</span><span class="sxs-lookup"><span data-stu-id="d711b-155">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="d711b-156">Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl**e **PararMacro** .</span><span class="sxs-lookup"><span data-stu-id="d711b-156">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="d711b-157">Essa macro deve ser anexada ao botão Revisar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="d711b-157">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d711b-158">Condição</span><span class="sxs-lookup"><span data-stu-id="d711b-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="d711b-159">Ação</span><span class="sxs-lookup"><span data-stu-id="d711b-159">Action</span></span></p></th>
<th><p><span data-ttu-id="d711b-160">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="d711b-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="d711b-161">Comentário</span><span class="sxs-lookup"><span data-stu-id="d711b-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="d711b-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-163"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-164">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="d711b-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d711b-165">ÉNulo ([ID do fornecedor])</span><span class="sxs-lookup"><span data-stu-id="d711b-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="d711b-166"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-167"><strong>Mensagem</strong>: mover para o registro do fornecedor cujos produtos você deseja ver, em seguida, clique no botão Revisar produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="d711b-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="d711b-168"><strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecione um fornecedor</span><span class="sxs-lookup"><span data-stu-id="d711b-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="d711b-169">Se não houver nenhum fornecedor atual no formulário fornecedores, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d711b-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d711b-170">...</span><span class="sxs-lookup"><span data-stu-id="d711b-170"></span></span></p></td>
<td><p><span data-ttu-id="d711b-171"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-172"><strong>Nome do controle</strong>: NomeDaEmpresa</span><span class="sxs-lookup"><span data-stu-id="d711b-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="d711b-173">Mova o foco para o controle NomeDaEmpresa.</span><span class="sxs-lookup"><span data-stu-id="d711b-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d711b-174">...</span><span class="sxs-lookup"><span data-stu-id="d711b-174"></span></span></p></td>
<td><p><span data-ttu-id="d711b-175"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d711b-176">Interrompa a macro.</span><span class="sxs-lookup"><span data-stu-id="d711b-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="d711b-177"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-178"><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>da lista de produto: <strong>DatasheetFilter nome</strong>: <strong>condição onde</strong>: [código do fornecedor] = [formulários]! Fornecedores! [SupplierID] <strong>Modo de dados</strong>: <strong>Modo de OnlyWindow de leitura</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-179">Abra o formulário de lista de produtos e mostram os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="d711b-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="d711b-180"><strong>Moveredimensionarjanela</strong></span><span class="sxs-lookup"><span data-stu-id="d711b-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="d711b-181"><strong>Direita</strong>: 0.7799&quot; <strong>para baixo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="d711b-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="d711b-182">Posiciona o formulário de lista de produtos no canto inferior direito do formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="d711b-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

