---
title: Ação da macro ExecutarComandodeMenu
TOCTitle: RunMenuCommand Macro Action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9d853c99fad322e17e8bbfd49cef27c14be33ffe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463860"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="3ef8a-102">Ação da macro ExecutarComandodeMenu</span><span class="sxs-lookup"><span data-stu-id="3ef8a-102">RunMenuCommand Macro Action</span></span>


<span data-ttu-id="3ef8a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ef8a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3ef8a-104">Você pode usar a ação **ExecutarComandodeMenu** para executar um comando interno do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ef8a-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="3ef8a-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="3ef8a-105">Setting</span></span>

<span data-ttu-id="3ef8a-106">A ação **ExecutarComandodeMenu** tem o argumento de ação a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ef8a-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ef8a-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="3ef8a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3ef8a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ef8a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ef8a-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="3ef8a-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="3ef8a-p101">O nome do comando a ser executado. A caixa <strong>Comando</strong> mostra os comandos internos disponíveis no Access, em ordem alfabética. Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3ef8a-p101">The name of the command you want to run. The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3ef8a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ef8a-113">Remarks</span></span>

<span data-ttu-id="3ef8a-114">Você pode usar a ação **ExecutarComandodeMenu** para executar um comando do Access em uma barra de menus personalizada, na barra de menus global, em um menu de atalho personalizado ou no menu de atalho global.</span><span class="sxs-lookup"><span data-stu-id="3ef8a-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="3ef8a-115">Use a ação **ExecutarComandodeMenu** em uma macro com expressões condicionais para executar um comando que dependa de certas condições.</span><span class="sxs-lookup"><span data-stu-id="3ef8a-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3ef8a-p102">[!OBSERVAçãO] Se você clicar na guia <STRONG>Arquivo</STRONG> e depois clicar em <STRONG>Recente</STRONG>, isso mostrará os bancos de dados usados mais recentemente. Você pode clicar em um desses bancos de dados em vez de clicar em <STRONG>Abrir</STRONG>. Esses itens de banco de dados não são exibidos na caixa de listagem suspensa do argumento <STRONG>Comando</STRONG> e não estão disponíveis quando a ação <STRONG>ExecutarComandodeMenu</STRONG> é usada em uma macro.</span><span class="sxs-lookup"><span data-stu-id="3ef8a-p102">Clicking the <STRONG>File</STRONG> tab and then clicking <STRONG>Recent</STRONG> shows the most recently used databases. You can click one of these databases instead of clicking <STRONG>Open</STRONG>. These database items don't appear in the drop-down list box for the <STRONG>Command</STRONG> argument, and aren't available by using the <STRONG>RunMenuCommand</STRONG> action in a macro.</span></span></P>



<span data-ttu-id="3ef8a-p103">Quando você converte um banco de dados do Access de uma versão anterior, alguns comandos talvez não fiquem mais disponíveis. Um comando pode ser renomeado, movido para outro menu ou deixar de estar disponível no Access. Não é possível converter as ações **ExecutarItemdoMenu** desses comandos em ações **ExecutarComandodeMenu**. Quando você abrir a macro, o Access exibirá uma ação **ExecutarComandodeMenu** com um argumento **Comando** em branco para esses argumentos. É preciso editar a macro e inserir um argumento de comando válido ou então excluir a ação **ExecutarComandodeMenu**.</span><span class="sxs-lookup"><span data-stu-id="3ef8a-p103">When you convert an Access database from a previous version of Access, some commands may no longer be available. A command may have been renamed, moved to a different menu, or may no longer be available in Access. The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions. When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands. You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="3ef8a-p104">Para executar a ação **ExecutarComandodeMenu** em um módulo do VBA(Visual Basic for Applications), use o método **ExecutarComando** do objeto **Application** (isso equivale ao método **ExecutarComando** do objeto **DoCmd** ).</span><span class="sxs-lookup"><span data-stu-id="3ef8a-p104">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object. (This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

