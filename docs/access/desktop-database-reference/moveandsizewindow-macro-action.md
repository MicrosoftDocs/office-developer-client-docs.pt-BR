---
title: Ação da macro MovereDimensionarJanela
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288803"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="af153-102">Ação da macro MovereDimensionarJanela</span><span class="sxs-lookup"><span data-stu-id="af153-102">MoveAndSizeWindow macro action</span></span>

<span data-ttu-id="af153-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af153-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af153-104">Se você tiver definido as opções de janela de documento para usar janelas sobrepostas em vez de documentos com guias, poderá usar a ação **moveredimensionarjanela** para mover ou redimensionar a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="af153-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="af153-105">Para obter informações sobre como definir as opções de janela de documento, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="af153-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="af153-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="af153-106">Setting</span></span>

<span data-ttu-id="af153-107">A ação **moveredimensionarjanela** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="af153-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af153-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="af153-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="af153-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="af153-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af153-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="af153-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-111">A nova posição horizontal do canto superior esquerdo da janela, medida a partir da extremidade esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="af153-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="af153-112">Insira a posição na caixa <strong>à direita</strong> na seção <strong>argumentos da ação</strong> do painel Construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="af153-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af153-113"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="af153-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-114">A nova posição vertical do canto superior esquerdo da janela, medida a partir da extremidade superior da janela.</span><span class="sxs-lookup"><span data-stu-id="af153-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af153-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="af153-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-116">A nova largura da janela.</span><span class="sxs-lookup"><span data-stu-id="af153-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af153-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="af153-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-118">A nova altura da janela.</span><span class="sxs-lookup"><span data-stu-id="af153-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="af153-119">Se você deixar um argumento em branco, o Microsoft Access usará a configuração atual da janela.</span><span class="sxs-lookup"><span data-stu-id="af153-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="af153-120">Você deve inserir um valor para pelo menos um argumento.</span><span class="sxs-lookup"><span data-stu-id="af153-120">You must enter a value for at least one argument.</span></span>

> [!NOTE]
> <span data-ttu-id="af153-121">Cada medida é em polegadas ou centímetros, dependendo das configurações regionais no painel de controle do Windows.</span><span class="sxs-lookup"><span data-stu-id="af153-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="af153-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="af153-122">Remarks</span></span>

<span data-ttu-id="af153-123">Para configurar um aplicativo para usar janelas sobrepostas em vez de documentos com guias, use o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="af153-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="af153-124">**Opções** de clique</span><span class="sxs-lookup"><span data-stu-id="af153-124">Click **Options**</span></span>

2.  <span data-ttu-id="af153-125">Clique em **banco de dados atual**.</span><span class="sxs-lookup"><span data-stu-id="af153-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="af153-126">Na seção **Opções do Aplicativo**, em **Opções de Janela de Documento**, clique em **Janelas Sobrepostas**.</span><span class="sxs-lookup"><span data-stu-id="af153-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="af153-127">Clique em **OK**e feche e reabra o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="af153-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="af153-128">Esta ação é semelhante a clicar em **mover** ou **dimensionar** no menu **controle** da janela.</span><span class="sxs-lookup"><span data-stu-id="af153-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="af153-129">Com os comandos de menu, você usa as teclas de seta do teclado para mover ou redimensionar a janela.</span><span class="sxs-lookup"><span data-stu-id="af153-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="af153-130">Com a ação **moveredimensionarjanela** , você insere as medidas de posição e de tamanho diretamente.</span><span class="sxs-lookup"><span data-stu-id="af153-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="af153-131">Você também pode usar o mouse para mover e dimensionar janelas.</span><span class="sxs-lookup"><span data-stu-id="af153-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="af153-132">Você pode usar essa ação em qualquer janela, em qualquer modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="af153-132">You can use this action on any window, in any view.</span></span>

> [!TIP]
> - <span data-ttu-id="af153-133">Para mover uma janela sem redimensioná-la, insira valores para os argumentos **Right** e **down** , mas deixe os argumentos **Width** e **Height** em branco.</span><span class="sxs-lookup"><span data-stu-id="af153-133">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>
> - <span data-ttu-id="af153-134">Para redimensionar uma janela sem movê-la, insira valores para os argumentos **Width** e **Height** , mas deixe os argumentos **Right** e **down** em branco.</span><span class="sxs-lookup"><span data-stu-id="af153-134">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="af153-135">Para executar a ação **moveredimensionarjanela** em um módulo do VBA (Visual Basic for Applications), use o método **MoverDimensionar** do objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="af153-135">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="af153-136">Exemplo</span><span class="sxs-lookup"><span data-stu-id="af153-136">Example</span></span>

<span data-ttu-id="af153-137">**Sincronizar formulários usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="af153-137">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="af153-138">A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="af153-138">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="af153-139">Ela mostra o uso das ações **eco**, **MessageBox**, **IrParaControle**, **PararMacro**, **AbrirFormulário**e **moveredimensionarjanela** .</span><span class="sxs-lookup"><span data-stu-id="af153-139">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="af153-140">Também mostra o uso de uma expressão condicional com as ações **MessageBox**, **IrParaControle**e **PararMacro** .</span><span class="sxs-lookup"><span data-stu-id="af153-140">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="af153-141">Essa macro deve ser anexada ao botão reVisar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="af153-141">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af153-142">Condição</span><span class="sxs-lookup"><span data-stu-id="af153-142">Condition</span></span></p></th>
<th><p><span data-ttu-id="af153-143">Ação</span><span class="sxs-lookup"><span data-stu-id="af153-143">Action</span></span></p></th>
<th><p><span data-ttu-id="af153-144">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="af153-144">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="af153-145">Comentário</span><span class="sxs-lookup"><span data-stu-id="af153-145">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="af153-146"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="af153-146"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-147"><strong>Echo ativado</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="af153-147"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-148">Interrompa a atualização da tela enquanto a macro estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="af153-148">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af153-149">Énulo ([código do fornecedor])</span><span class="sxs-lookup"><span data-stu-id="af153-149">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="af153-150"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="af153-150"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-151"><strong>Mensagem</strong>: mova para o registro de fornecedor cujos produtos você deseja ver e, em seguida, clique no botão revisar produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="af153-151"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="af153-152"><strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecionar um fornecedor</span><span class="sxs-lookup"><span data-stu-id="af153-152"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="af153-153">Se não houver um fornecedor atual no formulário fornecedores, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="af153-153">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="af153-154"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="af153-154"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-155"><strong>Nome do controle</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="af153-155"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="af153-156">Mover o foco para o controle CompanyName.</span><span class="sxs-lookup"><span data-stu-id="af153-156">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af153-157">...</span><span class="sxs-lookup"><span data-stu-id="af153-157"></span></span></p></td>
<td><p><span data-ttu-id="af153-158"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="af153-158"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="af153-159">Interrompa a macro.</span><span class="sxs-lookup"><span data-stu-id="af153-159">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="af153-160"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="af153-160"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-161"><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>de lista de produtos: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [CódigoDoFornecedor ID] = [formulários]! [Fornecedores]! [CódigoDoFornecedor] <strong>Modo de dados</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>normal</strong></span><span class="sxs-lookup"><span data-stu-id="af153-161"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-162">Abra o formulário lista de produtos e mostre os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="af153-162">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="af153-163"><strong>Moveredimensionarjanela</strong></span><span class="sxs-lookup"><span data-stu-id="af153-163"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="af153-164"><strong>direita</strong>: 0,7799&quot; <strong>baixo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="af153-164"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="af153-165">Posicione o formulário lista de produtos no canto inferior direito do formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="af153-165">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

