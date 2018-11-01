---
title: Ação da macro DefinirItemDoMenu
TOCTitle: SetMenuItem Macro Action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7a7de3d627dacfa0ca014a80ea037d0728220d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873562"
---
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="d1089-102">Ação da macro DefinirItemDoMenu</span><span class="sxs-lookup"><span data-stu-id="d1089-102">SetMenuItem Macro Action</span></span>


<span data-ttu-id="d1089-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1089-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1089-104">Use a ação **DefinirItemDoMenu** para definir o estado de itens de menu (habilitado ou desabilitado, selecionado ou não selecionado) em menus personalizados ou globais, na guia **Suplementos**.</span><span class="sxs-lookup"><span data-stu-id="d1089-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d1089-p101">[!OBSERVAçãO] A ação <STRONG>DefinirItemDoMenu</STRONG> funciona somente com menus personalizados e globais criados por macros de menu. A ação <STRONG>DefinirItemDoMenu</STRONG> está incluída no Microsoft Access somente para fins de compatibilidade com versões anteriores. Ela não funciona com a funcionalidade da barra de comandos, No entanto, você pode usar as propriedades <STRONG>Habilitado</STRONG> e <STRONG>Estado</STRONG> em um módulo do VBA (Visual Basic for Applications) para habilitar ou desabilitar e selecionar ou cancelar a seleção de itens em menus de atalho ou em menus personalizados ou globais.</span><span class="sxs-lookup"><span data-stu-id="d1089-p101">The <STRONG>SetMenuItem</STRONG> action works only with custom and global menus created by using menu macros. The <STRONG>SetMenuItem</STRONG> action is included in Microsoft Access only for compatibility with previous versions. It does not work with the command bar functionality. However, you can use the <STRONG>Enabled</STRONG> and <STRONG>State</STRONG> properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span></P>



## <a name="setting"></a><span data-ttu-id="d1089-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="d1089-109">Setting</span></span>

<span data-ttu-id="d1089-110">A ação **DefinirItemDoMenu** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d1089-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d1089-111">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="d1089-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d1089-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1089-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1089-113"><strong>Índice de menu</strong></span><span class="sxs-lookup"><span data-stu-id="d1089-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="d1089-114">O índice do menu que contém o comando para o qual você deseja definir o estado.</span><span class="sxs-lookup"><span data-stu-id="d1089-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="d1089-115">Insira um valor inteiro, começando com 0, para o índice do menu desejado no menu personalizado ou global.</span><span class="sxs-lookup"><span data-stu-id="d1089-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="d1089-116">Insira o valor de índice na caixa de <strong>Índice de Menu</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="d1089-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="d1089-117">O índice está em relação à posição do menu da macro do menu para o menu personalizado ou global (a posição desta ação <strong>AdicionarMenu</strong> da macro do menu, contado a partir de 0).</span><span class="sxs-lookup"><span data-stu-id="d1089-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="d1089-118">A exibição do menu pode ser um pouco diferente, porque você pode usar expressões condicionais da macro do menu para ocultar ou exibir itens de menu personalizado.</span><span class="sxs-lookup"><span data-stu-id="d1089-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="d1089-119">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d1089-119">This is a required argument.</span></span> <span data-ttu-id="d1089-120">Se você seleciona um menu com este argumento e deixar os argumentos <strong>Índice de comando</strong> e <strong>Índice de subcomando</strong> em branco, é possível habilitar ou desabilitar o nome do menu propriamente dito.</span><span class="sxs-lookup"><span data-stu-id="d1089-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="d1089-121">No entanto, você não pode selecionar ou desmarcar um nome de menu (o Access ignora as configurações da <strong>seleção</strong> e <strong>desmarque o</strong> do argumento <strong>sinalizador</strong> para nomes de menu).</span><span class="sxs-lookup"><span data-stu-id="d1089-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1089-122"><strong>Índice de comando</strong></span><span class="sxs-lookup"><span data-stu-id="d1089-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="d1089-p103">O índice do comando para o qual você deseja definir o estado. Insira um valor inteiro, começando em 0, para o índice do comando desejado no menu selecionado pelo argumento <strong>Índice de menu</strong>. O índice é relativo à posição do comando no grupo de macros que define o menu selecionado do menu personalizado ou global (a posição da macro desse comando no grupo de macros, contando de 0). A exibição do menu pode ser ligeiramente diferente, porque você pode usar expressões condicionais no grupo de macros do menu para ocultar ou exibir os comandos do menu personalizado.</span><span class="sxs-lookup"><span data-stu-id="d1089-p103">The index of the command for which you want to set the state. Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument. The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0). The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1089-127"><strong>Índice de subcomando</strong></span><span class="sxs-lookup"><span data-stu-id="d1089-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="d1089-p104">O índice do subcomando para o qual você deseja definir o estado. Isso só será aplicável se o comando desejado tiver um submenu. Insira um valor inteiro, começando em 0, para o índice do subcomando desejado no submenu selecionado pelo argumento <strong>Índice de comando</strong>. O índice é relativo à posição do subcomando no grupo de macros que define o submenu selecionado do menu personalizado ou global (a posição da macro desse subcomando no grupo de macros, contando de 0).</span><span class="sxs-lookup"><span data-stu-id="d1089-p104">The index of the subcommand for which you want to set the state. This applies only if the desired command has a submenu. Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument. The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1089-132"><strong>Flag</strong></span><span class="sxs-lookup"><span data-stu-id="d1089-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="d1089-p105">O estado para o qual você deseja definir o comando ou o subcomando. Clique em <strong>Cinza</strong> (para desabilitar o comando — ele ficará esmaecido), em <strong>Anular Cinza</strong> (para habilitá-lo), em <strong>Marcar</strong> (para colocar uma marca no comando — geralmente indicando que ele foi selecionado ou alternado) ou em <strong>Desmarcar</strong> (para remover a marca). O padrão é <strong>Anular Cinza</strong>.</span><span class="sxs-lookup"><span data-stu-id="d1089-p105">The state you want to set the command or subcommand to. Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check). The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d1089-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1089-136">Remarks</span></span>

<span data-ttu-id="d1089-p106">A ação **DefinirItemDoMenu** funciona somente em um menu personalizado ou global. Se a janela ativa não tiver um menu personalizado ou global, a execução de uma macro contendo a ação **DefinirItemDoMenu** causará um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d1089-p106">The **SetMenuItem** action works only on a custom or global menu. If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="d1089-139">Você pode usar essa ação para definir o estado de comandos e subcomandos de menu, mas não de subcomandos de subcomandos.</span><span class="sxs-lookup"><span data-stu-id="d1089-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="d1089-140">Para executar a ação **DefinirItemDoMenu** em um módulo do VBA (Visual Basic for Applications), use o método **SetMenuItem** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d1089-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

