---
title: Ação da macro ExecutarComandodeMenu
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c2b5a19b7a92fb68dfb774afeec5cd6ba456f38d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306500"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="dba3f-102">Ação da macro ExecutarComandodeMenu</span><span class="sxs-lookup"><span data-stu-id="dba3f-102">RunMenuCommand macro action</span></span>

<span data-ttu-id="dba3f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dba3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dba3f-104">Você pode usar a ação **ExecutarComandodeMenu** para executar um comando interno do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dba3f-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="dba3f-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="dba3f-105">Setting</span></span>

<span data-ttu-id="dba3f-106">A ação **ExecutarComandodeMenu** tem o argumento de ação a seguir.</span><span class="sxs-lookup"><span data-stu-id="dba3f-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dba3f-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="dba3f-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dba3f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="dba3f-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dba3f-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="dba3f-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="dba3f-p101">O nome do comando a ser executado. A caixa <strong>Comando</strong> mostra os comandos internos disponíveis no Access, em ordem alfabética. Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="dba3f-p101">The name of the command you want to run. The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="dba3f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="dba3f-113">Remarks</span></span>

<span data-ttu-id="dba3f-114">Você pode usar a ação **ExecutarComandodeMenu** para executar um comando do Access em uma barra de menus personalizada, na barra de menus global, em um menu de atalho personalizado ou no menu de atalho global.</span><span class="sxs-lookup"><span data-stu-id="dba3f-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="dba3f-115">Use a ação **ExecutarComandodeMenu** em uma macro com expressões condicionais para executar um comando que dependa de certas condições.</span><span class="sxs-lookup"><span data-stu-id="dba3f-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>

> [!NOTE]
> <span data-ttu-id="dba3f-p102">[!OBSERVAçãO] Se você clicar na guia **Arquivo** e depois clicar em **Recente**, isso mostrará os bancos de dados usados mais recentemente. Você pode clicar em um desses bancos de dados em vez de clicar em **Abrir**. Esses itens de banco de dados não são exibidos na caixa de listagem suspensa do argumento **Comando** e não estão disponíveis quando a ação **ExecutarComandodeMenu** é usada em uma macro.</span><span class="sxs-lookup"><span data-stu-id="dba3f-p102">Clicking the **File** tab and then clicking **Recent** shows the most recently used databases. You can click one of these databases instead of clicking **Open**. These database items don't appear in the drop-down list box for the **Command** argument, and aren't available by using the **RunMenuCommand** action in a macro.</span></span>

<span data-ttu-id="dba3f-p103">Quando você converte um banco de dados do Access de uma versão anterior, alguns comandos talvez não fiquem mais disponíveis. Um comando pode ser renomeado, movido para outro menu ou deixar de estar disponível no Access. Não é possível converter as ações **ExecutarItemdoMenu** desses comandos em ações **ExecutarComandodeMenu**. Quando você abrir a macro, o Access exibirá uma ação **ExecutarComandodeMenu** com um argumento **Comando** em branco para esses argumentos. É preciso editar a macro e inserir um argumento de comando válido ou então excluir a ação **ExecutarComandodeMenu**.</span><span class="sxs-lookup"><span data-stu-id="dba3f-p103">When you convert an Access database from a previous version of Access, some commands may no longer be available. A command may have been renamed, moved to a different menu, or may no longer be available in Access. The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions. When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands. You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="dba3f-p104">Para executar a ação **ExecutarComandodeMenu** em um módulo do VBA(Visual Basic for Applications), use o método **ExecutarComando** do objeto **Application** (isso equivale ao método **ExecutarComando** do objeto **DoCmd** ).</span><span class="sxs-lookup"><span data-stu-id="dba3f-p104">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object. (This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

