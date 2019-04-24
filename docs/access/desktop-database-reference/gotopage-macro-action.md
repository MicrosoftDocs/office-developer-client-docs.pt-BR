---
title: Ação da macro IrParaPágina
TOCTitle: GoToPage macro action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 10d55b435a59594eaf3e8380b6690ebbda63a258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292157"
---
# <a name="gotopage-macro-action"></a><span data-ttu-id="8fad0-102">Ação da macro IrParaPágina</span><span class="sxs-lookup"><span data-stu-id="8fad0-102">GoToPage macro action</span></span>

<span data-ttu-id="8fad0-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fad0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8fad0-p101">Você pode usar a ação **IrParaPágina** para mover o foco no formulário ativo para o primeiro controle em uma página especificada. É possível usar esta ação se você criou um formulário com quebras de páginas que contém grupos de informações relacionadas. Por exemplo, talvez haja um formulário Funcionários com informações pessoais em uma página, informações de escritório em outra e informações de vendas em uma terceira página. Você pode usar a ação **IrParaPágina** para se mover para a página desejada. Também pode apresentar várias páginas de informações em um único formulário usando controles guia.</span><span class="sxs-lookup"><span data-stu-id="8fad0-p101">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page. You can use this action if you have created a form with page breaks that contains groups of related information. For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page. You can use the **GoToPage** action to move to the desired page. You can also present multiple pages of information on a single form by using tab controls.</span></span>

## <a name="setting"></a><span data-ttu-id="8fad0-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="8fad0-109">Setting</span></span>

<span data-ttu-id="8fad0-110">A ação **IrParaPágina** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="8fad0-110">The **GoToPage** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8fad0-111">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="8fad0-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8fad0-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8fad0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8fad0-113"><strong>Número de página</strong></span><span class="sxs-lookup"><span data-stu-id="8fad0-113"><strong>Page Number</strong></span></span></p></td>
<td><p><span data-ttu-id="8fad0-p102">O número da página para a qual você deseja mover o foco. Insira o número de página na caixa <strong>Número de Página</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Se você deixar este argumento em branco, o foco continuará na página atual. É possível usar os argumentos <strong>À Direita</strong> e <strong>Abaixo</strong> para exibir a parte da página que deseja ver.</span><span class="sxs-lookup"><span data-stu-id="8fad0-p102">The number of the page to which you want to move the focus. Enter the page number in the <strong>Page Number</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. If you leave this argument blank, the focus stays on the current page. You can use the <strong>Right</strong> and <strong>Down</strong> arguments to display the part of the page you want to see.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fad0-118"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="8fad0-118"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="8fad0-p103">A posição horizontal do local da página, medida a partir da borda esquerda da janela que a contém, que aparecerá na borda esquerda da janela. Ela será obrigatória se você especificar um argumento <strong>Abaixo</strong>.</span><span class="sxs-lookup"><span data-stu-id="8fad0-p103">The horizontal position of the spot on the page, measured from the left edge of its containing window, that is to appear at the left edge of the window. This is required if you specify a <strong>Down</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fad0-121"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="8fad0-121"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="8fad0-p104">A posição vertical do local da página, medida a partir da borda superior da janela que a contém, que aparecerá na borda superior da janela. Ela será obrigatória se você especificar um argumento <strong>À Direita</strong>.</span><span class="sxs-lookup"><span data-stu-id="8fad0-p104">The vertical position of the spot on the page, measured from the top edge of its containing window, that is to appear at the top edge of the window. This is required if you specify a <strong>Right</strong> argument.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8fad0-124">Os argumentos **À Direita** e **Abaixo** são medidos em polegadas ou centímetros, dependendo das configurações regionais do Painel de Controle do Windows.</span><span class="sxs-lookup"><span data-stu-id="8fad0-124">The **Right** and **Down** arguments are measured in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fad0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fad0-125">Remarks</span></span>

<span data-ttu-id="8fad0-p105">Você pode usar esta ação para selecionar o primeiro controle (conforme definido pela ordem de tabulação do formulário) na página especificada. Use a ação **IrParaControle** para se mover para um controle específico no formulário.</span><span class="sxs-lookup"><span data-stu-id="8fad0-p105">You can use this action to select the first control (as defined by the form's tab order) on the specified page. Use the **GoToControl** action to move to a particular control on the form.</span></span>

<span data-ttu-id="8fad0-128">Você pode usar os argumentos **Right** e **down** para formulários com páginas maiores do que a janela do Access.</span><span class="sxs-lookup"><span data-stu-id="8fad0-128">You can use the **Right** and **Down** arguments for forms with pages larger than the Access window.</span></span> <span data-ttu-id="8fad0-129">Use o argumento **Número de Página** para se mover para a página desejada e use os argumentos **À Direita** e **Abaixo** para exibir a parte da página que deseja ver.</span><span class="sxs-lookup"><span data-stu-id="8fad0-129">Use the **Page Number** argument to move to the desired page, and then use the **Right** and **Down** arguments to display the part of the page you want to see.</span></span> <span data-ttu-id="8fad0-130">O Access exibe a parte da página cujo canto superior esquerdo está deslocado na distância especificada a partir do canto superior esquerdo da página.</span><span class="sxs-lookup"><span data-stu-id="8fad0-130">Access displays the part of the page whose upper-left corner is offset the specified distance from the upper-left corner of the page.</span></span>

<span data-ttu-id="8fad0-131">Não use a ação **IrParaPágina** nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="8fad0-131">You can't use the **GoToPage** action in the following cases:</span></span>

- <span data-ttu-id="8fad0-132">Para mover o foco para uma página em um formulário oculto.</span><span class="sxs-lookup"><span data-stu-id="8fad0-132">To move the focus to a page on a hidden form.</span></span>

- <span data-ttu-id="8fad0-133">Para mover o foco de uma página para outra em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="8fad0-133">To move the focus from one page to another within the tab control.</span></span>

<span data-ttu-id="8fad0-134">Para executar a ação **IrParaPágina** em um módulo do VBA (Visual Basic for Applications), use o método **GoToPage** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="8fad0-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span></span>

