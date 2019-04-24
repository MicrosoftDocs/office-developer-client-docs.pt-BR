---
title: Ação da macro DefinirAvisos
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308656"
---
# <a name="setwarnings-macro-action"></a><span data-ttu-id="4a981-102">Ação da macro DefinirAvisos</span><span class="sxs-lookup"><span data-stu-id="4a981-102">SetWarnings macro action</span></span>

<span data-ttu-id="4a981-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a981-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a981-104">Use a ação **DefinirAvisos** para ativar ou desativar mensagens do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a981-104">You can use the **SetWarnings** action to turn system messages on or off.</span></span>

> [!NOTE]
> <span data-ttu-id="4a981-105">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="4a981-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="4a981-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="4a981-106">Setting</span></span>

<span data-ttu-id="4a981-107">A ação **DefinirAvisos** tem o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a981-107">The **SetWarnings** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a981-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="4a981-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4a981-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a981-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a981-110"><strong>Avisos ativos</strong></span><span class="sxs-lookup"><span data-stu-id="4a981-110"><strong>Warnings On</strong></span></span></p></td>
<td><p><span data-ttu-id="4a981-p101">Especifica se as mensagens do sistema são exibidas. Clique em <strong>Sim</strong> (para ativar mensagens do sistema) ou em <strong>Não</strong> (para desativar mensagens do sistema) na caixa <strong>Avisos ativos</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Não</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a981-p101">Specifies whether system messages are displayed. Click <strong>Yes</strong> (to turn on system messages) or <strong>No</strong> (to turn off system messages) in the <strong>Warnings On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane. The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4a981-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a981-114">Remarks</span></span>

<span data-ttu-id="4a981-p102">Você pode usar esta ação para impedir que avisos e caixas de mensagem modais parem a macro. Entretanto, as mensagens de erro serão sempre exibidas. Além disso, o Microsoft Access exibirá todas as caixas de diálogo que exigirem outras entradas que não sejam uma simples escolha de botão (como **OK**, **Cancelar**, **Sim** ou **Não**)  por exemplo, qualquer caixa de diálogo que exija a entrada de texto ou a seleção de uma entre várias opções.</span><span class="sxs-lookup"><span data-stu-id="4a981-p102">You can use this action to prevent modal warnings and message boxes from stopping the macro. However, error messages are always displayed. Also, Microsoft Access displays any dialog boxes that require input other than just choosing a button (such as **OK**, **Cancel**, **Yes**, or **No**) — for example, any dialog box that requires you to enter text or select one of several options.</span></span>

<span data-ttu-id="4a981-p103">A execução desta ação com o argumento **Avisos ativos** definido como **Não** tem o mesmo efeito de pressionar ENTER sempre que um aviso ou caixa de mensagem é exibido. Geralmente, o botão **OK** ou **Sim** é escolhido em resposta ao aviso ou à mensagem.</span><span class="sxs-lookup"><span data-stu-id="4a981-p103">Carrying out this action with the **Warnings On** argument set to **No** has the same effect as pressing ENTER whenever a warning or message box is displayed. Typically, an **OK** or **Yes** button is chosen in response to the warning or message.</span></span>

<span data-ttu-id="4a981-120">Quando a macro é concluída, o Access reativa automaticamente a exibição de mensagens do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a981-120">When the macro finishes, Access automatically turns the display of system messages back on.</span></span>

<span data-ttu-id="4a981-p104">Em geral, a ação **Eco** é utilizada, o que oculta os resultados de uma macro até que ela esteja concluída. Você também pode usar a ação **DefinirAvisos** para ocultar avisos e caixas de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4a981-p104">Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished. You can use the **SetWarnings** action to hide the warnings and message boxes as well.</span></span>

> [!WARNING]
> <span data-ttu-id="4a981-p105">[!CUIDADO] Embora a ação **DefinirAvisos** possa simplificar as interações com as macros, tenha muito cuidado ao desativar mensagens do sistema. Em algumas situações, a interrupção de uma macro poderá ser conveniente se uma mensagem de aviso for exibida. A menos que você confie no resultado de todas as ações de macro, evite o uso desta ação.</span><span class="sxs-lookup"><span data-stu-id="4a981-p105">Although the **SetWarnings** action can simplify interactions with macros, you must be careful about turning system messages off. In some situations, you won't want to continue a macro if a certain warning message is displayed. Unless you're confident of the outcome of all macro actions, you should avoid using this action.</span></span>

<span data-ttu-id="4a981-126">Para executar a ação **DefinirAvisos** em um módulo do VBA (Visual Basic for Applications), use o método **SetWarnings** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="4a981-126">To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.</span></span>

