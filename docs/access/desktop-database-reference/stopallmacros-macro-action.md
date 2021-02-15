---
title: Ação da macro PararTodasMacros
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4e44182dd4290b05a2cfc8fabdf9240819f4b7aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314473"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="896d5-102">Ação da macro PararTodasMacros</span><span class="sxs-lookup"><span data-stu-id="896d5-102">StopAllMacros macro action</span></span>


<span data-ttu-id="896d5-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="896d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="896d5-104">Você pode usar a ação **PararTodasMacros** para interromper todas as macros em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="896d5-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="896d5-105">Setting</span><span class="sxs-lookup"><span data-stu-id="896d5-105">Setting</span></span>

<span data-ttu-id="896d5-106">A ação **PararTodasMacros** não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="896d5-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="896d5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="896d5-107">Remarks</span></span>

<span data-ttu-id="896d5-p101">Esta ação geralmente é usada quando uma condição de erro torna necessário parar todas as macros. Você pode usar uma expressão condicional na linha de ação da macro, contendo essa ação. Quando a expressão avaliar como **True** (–1), o Microsoft Access interromperá todas as macros.</span><span class="sxs-lookup"><span data-stu-id="896d5-p101">You typically use this action when an error condition makes it necessary to stop all macros. You can use a conditional expression in the macro's action row that contains this action. When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="896d5-p102">Por exemplo, você pode ter uma macro que exiba uma caixa de mensagem como uma de muitas ações complexas, incluindo a execução de outras macros. Se o usuário clicar em **Cancelar** nessa caixa de mensagem, a ação **PararTodasMacros** poderá interromper todas as macros em execução.</span><span class="sxs-lookup"><span data-stu-id="896d5-p102">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros. If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="896d5-113">Se uma macro tiver usado as ações **Eco** ou **DefinirAvisos** para desativar o eco ou a exibição de mensagens do sistema, a ação **PararTodasMacros** fará a reativação automaticamente.</span><span class="sxs-lookup"><span data-stu-id="896d5-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="896d5-114">Esta ação não está disponível em um módulo VBA (Visual Basic for Applications).</span><span class="sxs-lookup"><span data-stu-id="896d5-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

