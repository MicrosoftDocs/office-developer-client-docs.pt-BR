---
title: Ação da macro AdicionarMenu
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d04c98da0ecef1c2323930c74588b7a6a07c2e29
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026264"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="eb9e8-102">Ação da macro AdicionarMenu</span><span class="sxs-lookup"><span data-stu-id="eb9e8-102">AddMenu macro action</span></span>


<span data-ttu-id="eb9e8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb9e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb9e8-104">Este artigo descreve a operação básica da ação de macro **AdicionarMenu**.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="eb9e8-105">Use a ação **AdicionarMenu** para criar:</span><span class="sxs-lookup"><span data-stu-id="eb9e8-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="eb9e8-106">Menus personalizados na guia **Suplementos** de um formulário ou relatório específico.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="eb9e8-p101">Um menu de atalho personalizado de um formulário, relatório ou controle. O menu de atalho personalizado substitui o menu de atalho interno do formulário, relatório ou controle.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-p101">A custom shortcut menu for a form, report, or control. The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="eb9e8-p102">Um menu de atalho global. O menu de atalho global substitui o menu de atalho interno de campos em folhas de dados de consulta e tabela, formulários e relatórios, com exceção de onde foi adicionado um menu de atalho personalizado de um formulário, relatório ou controle.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-p102">A global shortcut menu. The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="eb9e8-111">Configuração</span><span class="sxs-lookup"><span data-stu-id="eb9e8-111">Setting</span></span>

<span data-ttu-id="eb9e8-112">A ação **AdicionarMenu** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb9e8-113">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="eb9e8-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="eb9e8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb9e8-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb9e8-115"><strong>Nome do Menu</strong></span><span class="sxs-lookup"><span data-stu-id="eb9e8-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="eb9e8-116">O nome do menu, por exemplo, &quot;comandos do relatório&quot; ou &quot;ferramentas&quot;.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="eb9e8-117">Para criar uma tecla de acesso para que você pode usar o teclado para escolher o menu, digite um e comercial (<strong>&amp;</strong>) antes da letra que farão parte a tecla de acesso.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="eb9e8-118">Essa letra será sublinhada no nome do menu na guia <strong>Suplementos</strong> .</span><span class="sxs-lookup"><span data-stu-id="eb9e8-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb9e8-119"><strong>Nome da Macro do Menu</strong></span><span class="sxs-lookup"><span data-stu-id="eb9e8-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="eb9e8-p104">O nome do grupo de macros que contém as macros dos comandos do menu. Esse é um argumento obrigatório. 

</span><span class="sxs-lookup"><span data-stu-id="eb9e8-p104">The name of the macro group that contains the macros for the menu's commands. This is a required argument.</span></span></p>
<p><span data-ttu-id="eb9e8-122"><strong>Observação</strong>: se você executar uma macro que contém a ação <strong>AdicionarMenu</strong> em um banco de dados biblioteca, Microsoft Office Access 2007 procurará o grupo de macros com esse nome de banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-122"><strong>NOTE</strong>: If you run a macro containing the <strong>AddMenu</strong> action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb9e8-123"><strong>Texto da Barra de Status</strong></span><span class="sxs-lookup"><span data-stu-id="eb9e8-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="eb9e8-p105">O texto que será exibido na barra de status quando o menu for selecionado. Este argumento é ignorado para menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-p105">The text to display in the status bar when the menu is selected. This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="eb9e8-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb9e8-126">Remarks</span></span>

<span data-ttu-id="eb9e8-p106">Para executar a ação **AdicionarMenu** em um módulo do VBA (Visual Basic for Applications), use o método **AddMenu** do objeto **DoCmd**. Você também pode definir a propriedade **BarraDeMenu** ou **ShortcutMenuBar** do VBA para criar um menu personalizado na guia **Suplementos** ou anexar um menu de atalho personalizado a um formulário, relatório ou controle. Defina a propriedade **ShortcutMenuBar** do objeto **Application** para criar um menu de atalho global.</span><span class="sxs-lookup"><span data-stu-id="eb9e8-p106">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object. You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control. You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

