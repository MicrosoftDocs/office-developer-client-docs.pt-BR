---
title: Ação da macro MostrarBarraDeFerramentas
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 01ba59ce0898068788adb9269b3203794d1f31d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306472"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="c1c80-102">Ação da macro MostrarBarraDeFerramentas</span><span class="sxs-lookup"><span data-stu-id="c1c80-102">ShowToolbar macro action</span></span>

<span data-ttu-id="c1c80-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1c80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1c80-104">Você pode usar a ação **MostrarBarraDeFerramentas** para exibir ou ocultar um grupo de comandos na guia **Suplementos**.</span><span class="sxs-lookup"><span data-stu-id="c1c80-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="c1c80-105">[!OBSERVAçãO] A ação **MostrarBarraDeFerramentas** não afeta os menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="c1c80-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="c1c80-106">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="c1c80-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="c1c80-107">Setting</span><span class="sxs-lookup"><span data-stu-id="c1c80-107">Setting</span></span>

<span data-ttu-id="c1c80-108">A ação **MostrarBarraDeFerramentas** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c1c80-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1c80-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="c1c80-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c1c80-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1c80-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1c80-111"><strong>Nome da barra de ferramentas</strong></span><span class="sxs-lookup"><span data-stu-id="c1c80-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c1c80-112">O nome do grupo de comandos na guia <strong>Suplementos</strong> a ser exibido ou ocultado.</span><span class="sxs-lookup"><span data-stu-id="c1c80-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="c1c80-113">A caixa <strong>Nome da Barra de Ferramentas</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros mostra todos os grupos disponíveis e que possam ser afetados por esta ação.</span><span class="sxs-lookup"><span data-stu-id="c1c80-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="c1c80-114">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c1c80-114">This is a required argument.</span></span> <span data-ttu-id="c1c80-115">Se você executar uma macro contendo a ação <strong>MostrarBarraDeFerramentas</strong> em um banco de dados biblioteca, o Access pesquisará o grupo com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="c1c80-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1c80-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="c1c80-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="c1c80-117">Especifica se o grupo deve ser exibido ou ocultado e em quais modos de exibição isso ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="c1c80-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="c1c80-118">O padrão é <strong>Sim</strong> (mostrar o grupo em todos os momentos).</span><span class="sxs-lookup"><span data-stu-id="c1c80-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="c1c80-119">Você pode selecionar <strong>Sim</strong> para sempre exibir o <strong>grupo,</strong> Onde Apropriado para exibir o grupo somente quando o formulário ou relatório apropriado estiver ativo ou <strong>Não</strong> para ocultar o grupo o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="c1c80-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c1c80-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1c80-120">Remarks</span></span>

<span data-ttu-id="c1c80-121">Esta ação pode ser usada em uma macro com expressões condicionais para exibir ou ocultar um grupo, dependendo de certas condições.</span><span class="sxs-lookup"><span data-stu-id="c1c80-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="c1c80-p103">Se você quiser mostrar um determinado grupo em apenas um formulário ou relatório, defina a propriedade **AoAtivar** do formulário ou do relatório usando o nome de uma macro que contenha uma ação **MostrarBarraDeFerramentas** para mostrar o grupo. Depois defina a propriedade **AoDesativar** do formulário ou do relatório usando o nome de uma macro que contenha a ação **MostrarBarraDeFerramentas** para ocultar o grupo.</span><span class="sxs-lookup"><span data-stu-id="c1c80-p103">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="c1c80-124">Não será possível exibir ou ocultar barras de ferramentas internas se a propriedade **AllowBuiltInToolbars** for definida como **False** (0) em um módulo do VBA (Visual Basic for Applications) ou se a opção **Allow Built-in Toolbars** for definida como **False** no VBA com o método **SetOption**.</span><span class="sxs-lookup"><span data-stu-id="c1c80-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="c1c80-125">Para executar a ação **MostrarBarraDeFerramentas** em um módulo do VBA, use o método **ShowToolbar** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="c1c80-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

