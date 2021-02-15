---
title: Ação de macro Eco (referência do banco de dados da área de trabalho do Access)
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
# <a name="echo-macro-action"></a><span data-ttu-id="89091-102">Ação da macro Eco</span><span class="sxs-lookup"><span data-stu-id="89091-102">Echo macro action</span></span>

<span data-ttu-id="89091-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89091-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89091-104">Você pode usar a **ação Eco** para especificar se o eco está ligado.</span><span class="sxs-lookup"><span data-stu-id="89091-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="89091-105">Por exemplo, você pode usar essa ação para ocultar ou mostrar os resultados de uma macro enquanto ela é executado.</span><span class="sxs-lookup"><span data-stu-id="89091-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="89091-106">Setting</span><span class="sxs-lookup"><span data-stu-id="89091-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="89091-107">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="89091-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="89091-108">A **ação Eco** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="89091-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89091-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="89091-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="89091-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="89091-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89091-111"><strong>Eco on</strong></span><span class="sxs-lookup"><span data-stu-id="89091-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-112">Clique <strong>em Sim</strong> (ativar eco) ou Não <strong></strong> (desativar eco) na caixa Eco Ligar na seção <strong>Argumentos</strong> da Ação do painel Construtor de Macros. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="89091-112">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="89091-113">O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="89091-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89091-114"><strong>Texto da Barra de Status</strong></span><span class="sxs-lookup"><span data-stu-id="89091-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-115">O texto a ser exibido na barra de status quando o eco está desligado.</span><span class="sxs-lookup"><span data-stu-id="89091-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="89091-116">Por exemplo, quando o eco está desligado, a barra de status pode exibir &quot; a macro que está sendo executado.&quot;</span><span class="sxs-lookup"><span data-stu-id="89091-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89091-117">Quando uma macro é executado, a atualização de tela geralmente mostra informações não essenciais para o funcionamento da macro.</span><span class="sxs-lookup"><span data-stu-id="89091-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="89091-118">Quando você definir o **argumento Eco Em** como **Não**, a macro será executado sem atualizar a tela.</span><span class="sxs-lookup"><span data-stu-id="89091-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="89091-119">Quando a macro termina, o Access readere o eco automaticamente e redesegue a janela.</span><span class="sxs-lookup"><span data-stu-id="89091-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="89091-120">A **configuração** Não para o argumento **Eco Em** não afeta a funcionalidade da macro ou seus resultados.</span><span class="sxs-lookup"><span data-stu-id="89091-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="89091-121">A **ação Eco** não suprime a exibição de caixas de diálogo modais, como mensagens de erro ou formulários pop-up, como folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="89091-121">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="89091-122">Você pode usar caixas de diálogo e formulários pop-up para coletar ou exibir informações, mesmo se o eco estiver desligado.</span><span class="sxs-lookup"><span data-stu-id="89091-122">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="89091-123">Para suprimir todas as caixas de diálogo ou mensagens, exceto caixas de mensagem de erro e caixas de diálogo que exigem que o usuário insira informações, use a ação **DefinirAvisos.**</span><span class="sxs-lookup"><span data-stu-id="89091-123">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="89091-124">Você pode executar a **ação Eco** mais de uma vez em uma macro.</span><span class="sxs-lookup"><span data-stu-id="89091-124">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="89091-125">Isso permite alterar o texto da barra de status enquanto a macro é executado.</span><span class="sxs-lookup"><span data-stu-id="89091-125">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="89091-126">Se você desativar o eco, poderá usar a ação **DisplayHourglassPointer** para alterar o ponteiro do mouse para um ícone de ampulheta (ou qualquer ícone de ponteiro do mouse definido para "Ocupado") para fornecer uma indicação visual de que a macro está em execução.</span><span class="sxs-lookup"><span data-stu-id="89091-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="89091-127">Para executar a **ação Eco** em um módulo do VBA (Visual Basic for Applications), use o método **Echo** do **objeto DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="89091-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="89091-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89091-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="89091-129">Definir o valor de um controle, usando uma macro</span><span class="sxs-lookup"><span data-stu-id="89091-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="89091-130">A macro a seguir abre o formulário Adicionar Produtos de um botão no formulário de Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="89091-130">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="89091-131">Mostra o uso das ações **Echo**, **CloseWindow**, **OpenForm**, **SetValue** e **GoToControl**.</span><span class="sxs-lookup"><span data-stu-id="89091-131">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="89091-132">A **ação SetValue** define o controle de ID do Fornecedor no formulário Produtos para o fornecedor atual no formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="89091-132">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="89091-133">A **ação IrParaControle** move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto.</span><span class="sxs-lookup"><span data-stu-id="89091-133">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="89091-134">Essa macro deve estar anexada ao botão Adicionar Produtos no formulário de Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="89091-134">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89091-135">Ação</span><span class="sxs-lookup"><span data-stu-id="89091-135">Action</span></span></p></th>
<th><p><span data-ttu-id="89091-136">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="89091-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="89091-137">Comentário</span><span class="sxs-lookup"><span data-stu-id="89091-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89091-138"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="89091-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-139"><strong>Echo On</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="89091-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-140">Interrompe a atualização de tela quando a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="89091-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89091-141"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="89091-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="89091-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-143">Fecha o Formulário de Lista de Produtos.</span><span class="sxs-lookup"><span data-stu-id="89091-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89091-144"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="89091-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="89091-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-146">Abre o formulário de produtos.</span><span class="sxs-lookup"><span data-stu-id="89091-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89091-147"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="89091-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="89091-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="89091-149">De definir o controle de ID de fornecedor para o fornecedor atual no formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="89091-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89091-150"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="89091-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-151"><strong>Control Name</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="89091-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="89091-152">Vá para o controle de ID da categoria.</span><span class="sxs-lookup"><span data-stu-id="89091-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="89091-153">Sincronizar formulários usando uma macro</span><span class="sxs-lookup"><span data-stu-id="89091-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="89091-154">A macro a seguir abre o formulário Lista de Produtos no canto inferior direito do formulário Fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="89091-154">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="89091-155">Ele mostra o uso das ações **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm** e **MoveAndSizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="89091-155">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="89091-156">Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl** e **StopMacro.**</span><span class="sxs-lookup"><span data-stu-id="89091-156">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="89091-157">Essa macro deve ser anexada ao botão Revisar Produtos no formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="89091-157">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89091-158">Condition</span><span class="sxs-lookup"><span data-stu-id="89091-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="89091-159">Ação</span><span class="sxs-lookup"><span data-stu-id="89091-159">Action</span></span></p></th>
<th><p><span data-ttu-id="89091-160">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="89091-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="89091-161">Comentário</span><span class="sxs-lookup"><span data-stu-id="89091-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="89091-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="89091-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-163"><strong>Echo On</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="89091-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-164">Interrompe a atualização de tela quando a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="89091-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89091-165">IsNull([ID do fornecedor])</span><span class="sxs-lookup"><span data-stu-id="89091-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="89091-166"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="89091-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-167"><strong>Mensagem:</strong>vá para o registro do fornecedor cujos produtos você deseja ver e clique no botão Revisar Produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="89091-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="89091-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span><span class="sxs-lookup"><span data-stu-id="89091-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="89091-169">Se não houver fornecedor atual no formulário Fornecedores, exibe uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="89091-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89091-170">...</span><span class="sxs-lookup"><span data-stu-id="89091-170">...</span></span></p></td>
<td><p><span data-ttu-id="89091-171"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="89091-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-172"><strong>Nome do controle</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="89091-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="89091-173">Mova o foco para o controle CompanyName.</span><span class="sxs-lookup"><span data-stu-id="89091-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89091-174">...</span><span class="sxs-lookup"><span data-stu-id="89091-174">...</span></span></p></td>
<td><p><span data-ttu-id="89091-175"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="89091-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="89091-176">Pare a macro.</span><span class="sxs-lookup"><span data-stu-id="89091-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="89091-177"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="89091-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-178"><strong>Nome do formulário</strong>: Exibição de Lista <strong>de</strong>Produtos : <strong>Nome do Filtro de</strong>Folha de Dados : <strong>Condição</strong>Onde : [ID do fornecedor] = [Formulários]! [Fornecedores]! [SupplierID] <strong>Modo de Dados</strong>: <strong>Ler Modo Somente Janela</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="89091-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-179">Abra o formulário Lista de Produtos e mostre os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="89091-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="89091-180"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="89091-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="89091-181"><strong>À</strong>direita: 0,7799 &quot; <strong>para baixo:</strong>1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="89091-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="89091-182">Posiciona o formulário Lista de Produtos no canto inferior direito do formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="89091-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

