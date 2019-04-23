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
localization_priority: Normal
ms.openlocfilehash: 119e824cae71d54bb398aa68f476a667f14a6888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280270"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="0e1b3-102">Ação da macro AdicionarMenu</span><span class="sxs-lookup"><span data-stu-id="0e1b3-102">AddMenu macro action</span></span>


<span data-ttu-id="0e1b3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e1b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e1b3-104">Este artigo descreve a operação básica da ação de macro **AdicionarMenu**.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="0e1b3-105">Use a ação **AdicionarMenu** para criar:</span><span class="sxs-lookup"><span data-stu-id="0e1b3-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="0e1b3-106">Menus personalizados na guia **Suplementos** de um formulário ou relatório específico.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="0e1b3-p101">Um menu de atalho personalizado de um formulário, relatório ou controle. O menu de atalho personalizado substitui o menu de atalho interno do formulário, relatório ou controle.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-p101">A custom shortcut menu for a form, report, or control. The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="0e1b3-p102">Um menu de atalho global. O menu de atalho global substitui o menu de atalho interno de campos em folhas de dados de consulta e tabela, formulários e relatórios, com exceção de onde foi adicionado um menu de atalho personalizado de um formulário, relatório ou controle.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-p102">A global shortcut menu. The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="0e1b3-111">Configuração</span><span class="sxs-lookup"><span data-stu-id="0e1b3-111">Setting</span></span>

<span data-ttu-id="0e1b3-112">A ação **AdicionarMenu** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e1b3-113">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="0e1b3-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0e1b3-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e1b3-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e1b3-115"><strong>Nome do Menu</strong></span><span class="sxs-lookup"><span data-stu-id="0e1b3-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1b3-116">O nome do menu, por exemplo &quot;, comandos&quot; ou &quot;ferramentas&quot;de relatório.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="0e1b3-117">Para criar uma chave de acesso para que você possa usar o teclado para escolher o menu, digite um e<strong>&amp;</strong>comercial () antes da letra que você deseja que seja a tecla de acesso.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="0e1b3-118">Essa letra estará sublinhada no nome do menu da guia <strong>Suplementos</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e1b3-119"><strong>Nome da Macro do Menu</strong></span><span class="sxs-lookup"><span data-stu-id="0e1b3-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1b3-120">O nome do grupo de macros que contém as macros dos comandos do menu.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-120">The name of the macro group that contains the macros for the menu's commands.</span></span> <span data-ttu-id="0e1b3-121">Esse é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-121">This is a required argument.</span></span></p>
<p><span data-ttu-id="0e1b3-122"><strong>Observação</strong>: se você executar uma macro que contém a ação <strong>AdicionarMenu</strong> em um banco de dados biblioteca, o Microsoft Office Access 2007 procurará o grupo de macros com esse nome somente no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-122"><strong>NOTE</strong>: If you run a macro containing the <strong>AddMenu</strong> action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e1b3-123"><strong>Texto da Barra de Status</strong></span><span class="sxs-lookup"><span data-stu-id="0e1b3-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="0e1b3-124">O texto que será exibido na barra de status quando o menu for selecionado.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-124">The text to display in the status bar when the menu is selected.</span></span> <span data-ttu-id="0e1b3-125">Este argumento é ignorado para menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-125">This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e1b3-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e1b3-126">Remarks</span></span>

<span data-ttu-id="0e1b3-p106">Para executar a ação **AdicionarMenu** em um módulo do VBA (Visual Basic for Applications), use o método **AddMenu** do objeto **DoCmd**. Você também pode definir a propriedade **BarraDeMenu** ou **ShortcutMenuBar** do VBA para criar um menu personalizado na guia **Suplementos** ou anexar um menu de atalho personalizado a um formulário, relatório ou controle. Defina a propriedade **ShortcutMenuBar** do objeto **Application** para criar um menu de atalho global.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-p106">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object. You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control. You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

