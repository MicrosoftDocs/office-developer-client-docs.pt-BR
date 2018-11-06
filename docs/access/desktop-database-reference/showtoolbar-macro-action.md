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
ms.openlocfilehash: ed69a84f9b1774b7c33711a0bb8e80da54e656cc
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997927"
---
# <a name="showtoolbar-macro-action"></a><span data-ttu-id="ab3d1-102">Ação da macro MostrarBarraDeFerramentas</span><span class="sxs-lookup"><span data-stu-id="ab3d1-102">ShowToolbar macro action</span></span>

<span data-ttu-id="ab3d1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab3d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab3d1-104">Você pode usar a ação **MostrarBarraDeFerramentas** para exibir ou ocultar um grupo de comandos na guia **Suplementos**.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-104">You can use the **ShowToolbar** action to display or hide a group of commands on the **Add-Ins** tab.</span></span>

> [!NOTE]
> - <span data-ttu-id="ab3d1-105">[!OBSERVAçãO] A ação **MostrarBarraDeFerramentas** não afeta os menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-105">The **ShowToolbar** action does not affect shortcut menus.</span></span>
> - <span data-ttu-id="ab3d1-106">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="ab3d1-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="ab3d1-107">Setting</span></span>

<span data-ttu-id="ab3d1-108">A ação **MostrarBarraDeFerramentas** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-108">The **ShowToolbar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab3d1-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="ab3d1-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ab3d1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab3d1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab3d1-111"><strong>Nome da barra de ferramentas</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d1-111"><strong>Toolbar Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ab3d1-112">O nome do grupo de comando na guia <strong>Suplementos</strong> que você deseja exibir ou ocultar.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-112">The name of the command group on the <strong>Add-Ins</strong> tab you want to display or hide.</span></span> <span data-ttu-id="ab3d1-113">A caixa <strong>Nome da barra de ferramentas</strong> na seção <strong>Argumentos da ação</strong> do painel do construtor de Macro mostra todos os grupos disponíveis que podem ser afetados por essa ação.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-113">The <strong>Toolbar Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane shows all the available groups that can be affected by this action.</span></span> <span data-ttu-id="ab3d1-114">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-114">This is a required argument.</span></span> <span data-ttu-id="ab3d1-115">Se você executar uma macro contendo a ação <strong>MostrarBarraDeFerramentas</strong> em um banco de dados biblioteca, o Access pesquisará o grupo com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-115">If you run a macro containing the <strong>ShowToolbar</strong> action in a library database, Access first looks for the group with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab3d1-116"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="ab3d1-116"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="ab3d1-117">Especifica para exibir ou ocultar o grupo e em quais modos de exibição para exibir ou ocultar a ele.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-117">Specifies whether to display or hide the group and in which views to display or hide it.</span></span> <span data-ttu-id="ab3d1-118">O padrão é <strong>Sim</strong> (Mostrar grupo sempre).</span><span class="sxs-lookup"><span data-stu-id="ab3d1-118">The default is <strong>Yes</strong> (show the group at all times).</span></span> <span data-ttu-id="ab3d1-119">Você pode selecionar <strong>Sim</strong> para exibir o grupo em todos os horários, <strong>Onde apropriado</strong> para exibir o grupo somente quando o formulário apropriado ou relatório estiver ativo, ou <strong>não</strong> para ocultar o grupo em todas as ocasiões.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-119">You can select <strong>Yes</strong> to display the group at all times, <strong>Where Appropriate</strong> to display the group only when the appropriate form or report is active, or <strong>No</strong> to hide the group at all times.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ab3d1-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab3d1-120">Remarks</span></span>

<span data-ttu-id="ab3d1-121">Esta ação pode ser usada em uma macro com expressões condicionais para exibir ou ocultar um grupo, dependendo de certas condições.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-121">You can use this action in a macro with conditional expressions to display or hide a group depending on certain conditions.</span></span>

<span data-ttu-id="ab3d1-p103">Se você quiser mostrar um determinado grupo em apenas um formulário ou relatório, defina a propriedade **AoAtivar** do formulário ou do relatório usando o nome de uma macro que contenha uma ação **MostrarBarraDeFerramentas** para mostrar o grupo. Depois defina a propriedade **AoDesativar** do formulário ou do relatório usando o nome de uma macro que contenha a ação **MostrarBarraDeFerramentas** para ocultar o grupo.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-p103">If you want to show a particular group on just one form or report, you can set the **OnActivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to show the group. Then set the **OnDeactivate** property of the form or report to the name of a macro that contains a **ShowToolbar** action to hide the group.</span></span>

<span data-ttu-id="ab3d1-124">Não será possível exibir ou ocultar barras de ferramentas internas se a propriedade **AllowBuiltInToolbars** for definida como **False** (0) em um módulo do VBA (Visual Basic for Applications) ou se a opção **Allow Built-in Toolbars** for definida como **False** no VBA com o método **SetOption**.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-124">The built-in toolbars are not available to display or hide by using this action if you set the **AllowBuiltInToolbars** property to **False** (0) in a Visual Basic for Applications (VBA) module, or if you set the **Allow Built-in Toolbars** option to **False** in VBA by using the **SetOption** method.</span></span>

<span data-ttu-id="ab3d1-125">Para executar a ação **MostrarBarraDeFerramentas** em um módulo do VBA, use o método **ShowToolbar** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="ab3d1-125">To run the **ShowToolbar** action in a VBA module, use the **ShowToolbar** method of the **DoCmd** object.</span></span>

