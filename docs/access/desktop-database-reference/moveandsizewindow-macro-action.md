---
title: Ação de Macro Moveredimensionarjanela
TOCTitle: MoveAndSizeWindow Macro Action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab2998140f46fd3275f564684995d9a4d8d56968
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882536"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="28552-102">Ação de Macro Moveredimensionarjanela</span><span class="sxs-lookup"><span data-stu-id="28552-102">MoveAndSizeWindow Macro Action</span></span>


<span data-ttu-id="28552-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="28552-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="28552-104">Se você tiver configurado as opções de janela para usar janelas sobrepostas, em vez de documentos com guias para seu documento, você pode usar a ação **Moveredimensionarjanela** para mover ou redimensionar a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="28552-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="28552-105">Para obter informações sobre como configurar opções da janela de documento, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="28552-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="28552-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="28552-106">Setting</span></span>

<span data-ttu-id="28552-107">A ação **Moveredimensionarjanela** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="28552-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28552-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="28552-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="28552-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="28552-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28552-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="28552-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-111">A nova posição horizontal do canto superior esquerdo da janela, medida a partir da extremidade esquerda da janela.</span><span class="sxs-lookup"><span data-stu-id="28552-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="28552-112">Insira a posição na caixa <strong>direita</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="28552-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28552-113"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="28552-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-114">A nova posição vertical do canto superior esquerdo da janela, medida a partir da extremidade superior da janela.</span><span class="sxs-lookup"><span data-stu-id="28552-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28552-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="28552-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-116">A nova largura da janela.</span><span class="sxs-lookup"><span data-stu-id="28552-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28552-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="28552-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-118">A nova altura da janela.</span><span class="sxs-lookup"><span data-stu-id="28552-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28552-119">Se você deixar um argumento em branco, o Microsoft Access usa a configuração atual da janela.</span><span class="sxs-lookup"><span data-stu-id="28552-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="28552-120">Você deve inserir um valor para pelo menos um argumento.</span><span class="sxs-lookup"><span data-stu-id="28552-120">You must enter a value for at least one argument.</span></span>


> [!NOTE]
> <P><span data-ttu-id="28552-121">Cada medida está em polegadas ou centímetros, dependendo das configurações regionais no painel de controle do Windows.</span><span class="sxs-lookup"><span data-stu-id="28552-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="28552-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="28552-122">Remarks</span></span>

<span data-ttu-id="28552-123">Para configurar um aplicativo para usar janelas sobrepostas, em vez de documentos com guias, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="28552-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="28552-124">e, em seguida, clique em **Opções**</span><span class="sxs-lookup"><span data-stu-id="28552-124">and then click **Options**</span></span>

2.  <span data-ttu-id="28552-125">Clique em **banco de dados atual**.</span><span class="sxs-lookup"><span data-stu-id="28552-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="28552-126">Na seção **Opções do Aplicativo**, em **Opções de Janela de Documento**, clique em **Janelas Sobrepostas**.</span><span class="sxs-lookup"><span data-stu-id="28552-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="28552-127">Clique em **Okey**e, em seguida, feche e reabra o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="28552-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="28552-128">Esta ação é semelhante a clicar em **Mover** ou **Dimensionar** , no menu **controle** da janela.</span><span class="sxs-lookup"><span data-stu-id="28552-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="28552-129">Com os comandos de menu, você pode usar teclas de direção do teclado para mover ou redimensionar a janela.</span><span class="sxs-lookup"><span data-stu-id="28552-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="28552-130">Com a ação **Moveredimensionarjanela** , insira as medidas de tamanho e posição diretamente.</span><span class="sxs-lookup"><span data-stu-id="28552-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="28552-131">Você também pode usar o mouse para mover e dimensionar janelas.</span><span class="sxs-lookup"><span data-stu-id="28552-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="28552-132">Você pode usar essa ação em qualquer janela, em qualquer modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="28552-132">You can use this action on any window, in any view.</span></span>

<span data-ttu-id="28552-133">**Dicas**</span><span class="sxs-lookup"><span data-stu-id="28552-133">**Tips**</span></span>

  - <span data-ttu-id="28552-134">Para mover uma janela sem redimensioná-la, insira valores para a **direita** e **para baixo** argumentos, mas deixar os argumentos **largura** e **Altura** em branco.</span><span class="sxs-lookup"><span data-stu-id="28552-134">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>

  - <span data-ttu-id="28552-135">Para redimensionar uma janela sem movê-lo, insira valores para a **largura** e **Altura** argumentos, mas deixar os argumentos **direita** e **para baixo** em branco.</span><span class="sxs-lookup"><span data-stu-id="28552-135">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="28552-136">Para executar a ação **Moveredimensionarjanela** em um módulo Visual Basic for Applications (VBA), use o método **MoveSize** do objeto **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="28552-136">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="28552-137">Exemplo</span><span class="sxs-lookup"><span data-stu-id="28552-137">Example</span></span>

<span data-ttu-id="28552-138">**Sincronizar formulários usando uma macro**</span><span class="sxs-lookup"><span data-stu-id="28552-138">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="28552-139">A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="28552-139">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="28552-140">Ela mostra o uso do **eco**, **MessageBox**, **GoToControl**, **PararMacro**, **AbrirFormulário**e **Moveredimensionarjanela** ações.</span><span class="sxs-lookup"><span data-stu-id="28552-140">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="28552-141">Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl**e **PararMacro** .</span><span class="sxs-lookup"><span data-stu-id="28552-141">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="28552-142">Essa macro deve ser anexada ao botão Revisar produtos no formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="28552-142">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28552-143">Condição</span><span class="sxs-lookup"><span data-stu-id="28552-143">Condition</span></span></p></th>
<th><p><span data-ttu-id="28552-144">Ação</span><span class="sxs-lookup"><span data-stu-id="28552-144">Action</span></span></p></th>
<th><p><span data-ttu-id="28552-145">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="28552-145">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="28552-146">Comentário</span><span class="sxs-lookup"><span data-stu-id="28552-146">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="28552-147"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="28552-147"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-148"><strong>Eco no</strong>: <strong>não</strong></span><span class="sxs-lookup"><span data-stu-id="28552-148"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-149">Pare a atualização da tela enquanto a macro é executada.</span><span class="sxs-lookup"><span data-stu-id="28552-149">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28552-150">ÉNulo ([ID do fornecedor])</span><span class="sxs-lookup"><span data-stu-id="28552-150">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="28552-151"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="28552-151"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-152"><strong>Mensagem</strong>: mover para o registro do fornecedor cujos produtos você deseja ver, em seguida, clique no botão Revisar produtos novamente.</span><span class="sxs-lookup"><span data-stu-id="28552-152"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="28552-153"><strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecione um fornecedor</span><span class="sxs-lookup"><span data-stu-id="28552-153"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="28552-154">Se não houver nenhum fornecedor atual no formulário fornecedores, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="28552-154">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="28552-155"><strong>IrParaControle</strong></span><span class="sxs-lookup"><span data-stu-id="28552-155"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-156"><strong>Nome do controle</strong>: NomeDaEmpresa</span><span class="sxs-lookup"><span data-stu-id="28552-156"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="28552-157">Mova o foco para o controle NomeDaEmpresa.</span><span class="sxs-lookup"><span data-stu-id="28552-157">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28552-158">...</span><span class="sxs-lookup"><span data-stu-id="28552-158"></span></span></p></td>
<td><p><span data-ttu-id="28552-159"><strong>PararMacro</strong></span><span class="sxs-lookup"><span data-stu-id="28552-159"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="28552-160">Interrompa a macro.</span><span class="sxs-lookup"><span data-stu-id="28552-160">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="28552-161"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="28552-161"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-162"><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>da lista de produto: <strong>DatasheetFilter nome</strong>: <strong>condição onde</strong>: [código do fornecedor] = [formulários]! Fornecedores! [SupplierID] <strong>Modo de dados</strong>: <strong>Modo de OnlyWindow de leitura</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="28552-162"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-163">Abra o formulário de lista de produtos e mostram os produtos do fornecedor atual.</span><span class="sxs-lookup"><span data-stu-id="28552-163">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="28552-164"><strong>Moveredimensionarjanela</strong></span><span class="sxs-lookup"><span data-stu-id="28552-164"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="28552-165"><strong>Direita</strong>: 0.7799&quot; <strong>para baixo</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="28552-165"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="28552-166">Posiciona o formulário de lista de produtos no canto inferior direito do formulário fornecedores.</span><span class="sxs-lookup"><span data-stu-id="28552-166">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

