---
title: Ação de Macro de eco (referência de banco de dados da área de trabalho do Access)
TOCTitle: Echo Macro Action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81fdb71631b4ba5afd8e22ca7640e6a98ff5c78f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462213"
---
# <a name="echo-macro-action"></a><span data-ttu-id="5c9ad-102">Ação de Macro eco</span><span class="sxs-lookup"><span data-stu-id="5c9ad-102">Echo Macro Action</span></span>


<span data-ttu-id="5c9ad-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c9ad-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5c9ad-104">Você pode usar a ação **eco** para especificar se o eco está ativado.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="5c9ad-105">Por exemplo, você pode usar essa ação para ocultar ou mostrar os resultados de uma macro enquanto ele é executado.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="5c9ad-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="5c9ad-106">Setting</span></span>


> [!NOTE]
> <P><span data-ttu-id="5c9ad-p102">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



<span data-ttu-id="5c9ad-109">A ação **eco** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-109">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c9ad-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="5c9ad-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5c9ad-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c9ad-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c9ad-112"><strong>Eco ativo</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-112"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-113">Clique em <strong>Sim</strong> (ativar o eco) ou <strong>não</strong> (desativar o eco) na caixa <strong>Eco na</strong> seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-113">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="5c9ad-114">O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-114">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c9ad-115"><strong>Texto da Barra de Status</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-115"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-116">O texto a ser exibido na barra quando o eco está desativado de status.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-116">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="5c9ad-117">Por exemplo, quando o eco está desativado, a barra de status pode exibir &quot;a macro está sendo executada.&quot;</span><span class="sxs-lookup"><span data-stu-id="5c9ad-117">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c9ad-118">Quando executa uma macro, muitas vezes mostra informações não essenciais ao funcionamento da macro de atualização de tela.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-118">When runs a macro, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="5c9ad-119">Quando você define o argumento **Echo ativo** como **não**, a macro será executada sem atualizar a tela.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-119">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="5c9ad-120">Quando a macro é concluída, o Access automaticamente ativa eco e redesenha a janela.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-120">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="5c9ad-121">A configuração **não** para o argumento **Eco ativo** não afeta a funcionalidade da macro ou seus resultados.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-121">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="5c9ad-122">A ação **Echo** não suprime a exibição de caixas de diálogo modal, mensagens de erro ou formulários pop-up, como folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-122">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="5c9ad-123">Você pode usar caixas de diálogo e formulários pop-up para coletar ou exibir informações, mesmo se o eco está desativado.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-123">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="5c9ad-124">Para suprimir todas as caixas de diálogo ou de mensagem, exceto as caixas de mensagem de erro e caixas de diálogo que exigem que o usuário insira informações, use a ação **DefinirAvisos** .</span><span class="sxs-lookup"><span data-stu-id="5c9ad-124">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="5c9ad-125">Você pode executar a ação **eco** mais de uma vez em uma macro.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-125">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="5c9ad-126">Isso permite que você altere o texto da barra de status enquanto a macro será executada.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-126">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="5c9ad-127">Se você desativar o eco, você pode usar a ação **Exibirponteirodeampulheta** para alterar o ponteiro do mouse em um ícone de ampulheta (ou qualquer outro ícone de ponteiro do mouse definido para "Ocupado") para fornecer uma indicação visual que a macro está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-127">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="5c9ad-128">Para executar a ação **eco** em um módulo Visual Basic for Applications (VBA), use o método **Echo** do objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="5c9ad-128">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="5c9ad-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c9ad-129">Examples</span></span>

<span data-ttu-id="5c9ad-130">**Definir o valor de um controle usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="5c9ad-130">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="5c9ad-131">A macro a seguir abre o formulário Adicionar produtos com um botão no formulário Suppliers.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-131">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="5c9ad-132">Ela mostra o uso do **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **GoToControl** ações.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-132">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="5c9ad-133">A ação **DefinirValor** define o controle de código do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-133">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="5c9ad-134">A ação **GoToControl** , em seguida, move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-134">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="5c9ad-135">Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-135">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c9ad-136">Ação</span><span class="sxs-lookup"><span data-stu-id="5c9ad-136">Action</span></span></p></th>
<th><p><span data-ttu-id="5c9ad-137">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="5c9ad-137">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="5c9ad-138">Comentário</span><span class="sxs-lookup"><span data-stu-id="5c9ad-138">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c9ad-139"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-139"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-140"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-140"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-141">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-141">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c9ad-142"><strong>FecharJanela</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-142"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-143"><strong>Tipo de objeto</strong>: <strong>Nome FormObject</strong>: lista de produto para <strong>Salvar</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-143"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-144">Feche o formulário de lista de produtos.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-144">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c9ad-145"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-145"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-146"><strong>Nome do formulário</strong>: produtos <strong>modo de exibição</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-146"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-147">Abra o formulário Products.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-147">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c9ad-148"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-148"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-149"><strong>Item</strong>: [formulários]! [Produtos]! [SupplierID] <strong>Expressão</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="5c9ad-149"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="5c9ad-150">Defina o controle de código do fornecedor como o fornecedor atual no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-150">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c9ad-151"><strong>IrParaControle</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-151"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-152"><strong>Nome do controle</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="5c9ad-152"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="5c9ad-153">Vá para o controle de ID da categoria.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-153">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c9ad-154">**Sincronizar formulários usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="5c9ad-154">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="5c9ad-155">A macro a seguir abre o formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-155">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="5c9ad-156">Ela mostra o uso do **eco**, **MessageBox**, **GoToControl**, **PararMacro**, **AbrirFormulário**e **Moveredimensionarjanela** ações.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-156">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="5c9ad-157">Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl**e **PararMacro** .</span><span class="sxs-lookup"><span data-stu-id="5c9ad-157">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="5c9ad-158">Essa macro deve ser anexada ao botão Revisar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-158">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c9ad-159">Condição</span><span class="sxs-lookup"><span data-stu-id="5c9ad-159">Condition</span></span></p></th>
<th><p><span data-ttu-id="5c9ad-160">Ação</span><span class="sxs-lookup"><span data-stu-id="5c9ad-160">Action</span></span></p></th>
<th><p><span data-ttu-id="5c9ad-161">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="5c9ad-161">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="5c9ad-162">Comentário</span><span class="sxs-lookup"><span data-stu-id="5c9ad-162">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5c9ad-163"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-163"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-164"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-164"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-165">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-165">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c9ad-166">ÉNulo ([ID do fornecedor])</span><span class="sxs-lookup"><span data-stu-id="5c9ad-166">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="5c9ad-167"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-167"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-168"><strong>Mensagem</strong>: mover para o registro do fornecedor cujos produtos você deseja ver, em seguida, clique no botão Revisar produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-168"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="5c9ad-169"><strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecione um fornecedor</span><span class="sxs-lookup"><span data-stu-id="5c9ad-169"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="5c9ad-170">Se não houver nenhum fornecedor atual no formulário fornecedores, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-170">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c9ad-171">...</span><span class="sxs-lookup"><span data-stu-id="5c9ad-171"></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-172"><strong>IrParaControle</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-172"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-173"><strong>Nome do controle</strong>: NomeDaEmpresa</span><span class="sxs-lookup"><span data-stu-id="5c9ad-173"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="5c9ad-174">Mova o foco para o controle NomeDaEmpresa.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-174">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c9ad-175">...</span><span class="sxs-lookup"><span data-stu-id="5c9ad-175"></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-176"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-176"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c9ad-177">Interrompa a macro.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-177">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5c9ad-178"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-178"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-179"><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>da lista de produto: <strong>DatasheetFilter nome</strong>: <strong>condição onde</strong>: [código do fornecedor] = [formulários]! Fornecedores! [SupplierID] <strong>Modo de dados</strong>: <strong>Modo de OnlyWindow de leitura</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-179"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-180">Abra o formulário de lista de produtos e mostram os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-180">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5c9ad-181"><strong>Moveredimensionarjanela</strong></span><span class="sxs-lookup"><span data-stu-id="5c9ad-181"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="5c9ad-182"><strong>Direita</strong>: 0.7799&quot; <strong>para baixo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="5c9ad-182"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="5c9ad-183">Posiciona o formulário de lista de produtos no canto inferior direito do formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-183">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

