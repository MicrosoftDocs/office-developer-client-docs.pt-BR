---
title: Ação da macro PassoÚnico
TOCTitle: SingleStep macro action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9e934b290472dc4bb0ad8619b2ada6992b4215c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308628"
---
# <a name="singlestep-macro-action"></a><span data-ttu-id="3ba18-102">Ação da macro PassoÚnico</span><span class="sxs-lookup"><span data-stu-id="3ba18-102">SingleStep macro action</span></span>

<span data-ttu-id="3ba18-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ba18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ba18-104">Use a ação **PassoAPasso** para pausar a execução da macro e abrir a caixa de diálogo **Macro Passo a Passo**.</span><span class="sxs-lookup"><span data-stu-id="3ba18-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="3ba18-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="3ba18-105">Setting</span></span>

<span data-ttu-id="3ba18-106">A ação **PassoAPasso** não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="3ba18-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba18-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ba18-107">Remarks</span></span>

- <span data-ttu-id="3ba18-p101">Use a ação **PassoAPasso** para solucionar problemas em uma macro que não esteja funcionando corretamente. Você pode adicionar a ação **PassoAPasso** a uma macro imediatamente antes de uma ação que você suspeite ser a causa do problema. A ação pausará a macro e abrirá a caixa de diálogo **Macro Passo a Passo**. Essa caixa de diálogo exibe informações sobre a ação da macro atual, como nome da macro, todas as condições especificadas, nome da ação, argumentos e, se aplicável, o número do erro. Na caixa de diálogo, clique em **Passo** para avançar para a próxima ação da macro, clique em **Parar Todas as Macros** para interromper a macro atual e todas as outras macros em execução ou clique em **Continuar** para interromper o passo a passo e continuar a operação normal da macro.</span><span class="sxs-lookup"><span data-stu-id="3ba18-p101">Use the **SingleStep** action to troubleshoot a macro that is not working properly. You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem. The action pauses the macro and opens the **Macro Single Step** dialog box. This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable. In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

- <span data-ttu-id="3ba18-p102">A ação **PassoAPasso** tem efeito similar a clicar em **Passo a Passo** no grupo **Ferramentas** da guia **Design** do Construtor de Macros. A diferença entre fazer isso e executar a ação **PassoAPasso** é que, ao executar a ação, você poderá colocar a ação da macro exatamente onde desejar que um passo a passo comece. Dessa forma, não é preciso passar por todas as ações anteriores para obter aquela que você deseja examinar. Por outro lado, quando você clica em **Passo a Passo** no Construtor de Macros, é preciso fazer isso antes de executar a macro. Nesse caso, o passo a passo começa na primeira ação da macro.</span><span class="sxs-lookup"><span data-stu-id="3ba18-p102">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder. The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin. That way, you don't have to step through all the previous actions to get to the one you want to examine. On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro. In that case, single stepping begins at the first action in the macro.</span></span>

> [!NOTE]
> <span data-ttu-id="3ba18-p103">[!OBSERVAçãO] Se você aplicar o passo a passo do início ao fim de uma macro, mas sem clicar em **Continuar**, o passo a passo ainda estará ativo quando a macro for finalizada. Qualquer macro subsequente que você executar será iniciada no modo passo a passo. Para desativar esse modo, clique em **Continuar** na caixa de diálogo **Macro Passo a Passo** ou, com uma macro aberta no modo de exibição de Design, na guia **Design** do grupo **Ferramentas**, clique em **Passo a Passo** para desmarcá-lo.</span><span class="sxs-lookup"><span data-stu-id="3ba18-p103">If you single-step all the way to the end of a macro without clicking **Continue**, single stepping will still be in effect when the macro ends. Any subsequent macro you run will start in single step mode. To turn off single stepping, either click **Continue** in the **Macro Single Step** dialog box, or, with a macro open in Design view, on the **Design** tab, in the **Tools** group, click **Single Step** so that it is no longer selected.</span></span>
