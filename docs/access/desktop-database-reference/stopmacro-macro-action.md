---
title: Ação da macro PararMacro
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308495"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="e6eb0-102">Ação da macro PararMacro</span><span class="sxs-lookup"><span data-stu-id="e6eb0-102">StopMacro macro action</span></span>

<span data-ttu-id="e6eb0-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6eb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6eb0-104">Você pode usar a ação **PararMacro** para interromper a macro em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="e6eb0-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="e6eb0-105">Setting</span></span>

<span data-ttu-id="e6eb0-106">A ação **PararMacro** não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6eb0-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6eb0-107">Remarks</span></span>

<span data-ttu-id="e6eb0-108">Normalmente, você usa esta ação quando uma condição torna necessário parar a macro.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="e6eb0-109">Você pode usar uma expressão condicional na linha de ação da macro, contendo essa ação.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="e6eb0-110">Quando a expressão é avaliada como **true** (– 1), o Microsoft Access interrompe a macro.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="e6eb0-111">Por exemplo, você pode criar uma macro que abre um formulário mostrando os totais de pedidos diários da data inserida em uma caixa de diálogo personalizada.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="e6eb0-112">Você pode usar uma expressão condicional para ter certeza de que o controle de **data da ordem** na caixa de diálogo contém uma data válida.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="e6eb0-113">Caso contrário, a ação **MessageBox** poderá exibir uma mensagem de erro e a ação **PararMacro** poderá interromper a macro.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="e6eb0-114">Se a macro tiver usado as ações **eco** ou SetWarnings para ativar o eco ou a exibição de mensagens do sistema, a ação **PararMacro** as ativará automaticamente. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e6eb0-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="e6eb0-115">Esta ação não está disponível em um módulo VBA (Visual Basic for Applications).</span><span class="sxs-lookup"><span data-stu-id="e6eb0-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="e6eb0-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e6eb0-116">Example</span></span>

<span data-ttu-id="e6eb0-117">A macro a seguir demonstra o uso da ação **AoOcorrerErro** .</span><span class="sxs-lookup"><span data-stu-id="e6eb0-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="e6eb0-118">Neste exemplo, a ação **AoOcorrerErro** especifica que o Access executa uma macro de tratamento de erros personalizada chamada ErrorHandler quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="e6eb0-119">Quando ocorre um erro, a submacro CatchErrors é chamada.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="e6eb0-120">Se o número de erro for 2102, uma mensagem específica é exibida e a execução da macro é interrompida.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="e6eb0-121">Caso contrário, uma mensagem descrevendo o erro é exibida e a macro é pausada para que você possa executar a solução de problemas adicional.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="e6eb0-122">A macro ErrorHandler exibe uma caixa de mensagem que se refere ao objeto **MacroError** para exibir informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="e6eb0-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="e6eb0-123">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e6eb0-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
