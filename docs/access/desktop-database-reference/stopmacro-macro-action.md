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
# <a name="stopmacro-macro-action"></a><span data-ttu-id="04cc9-102">Ação da macro PararMacro</span><span class="sxs-lookup"><span data-stu-id="04cc9-102">StopMacro macro action</span></span>

<span data-ttu-id="04cc9-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04cc9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04cc9-104">Você pode usar a **ação PararMacro** para interromper a macro em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="04cc9-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="04cc9-105">Setting</span><span class="sxs-lookup"><span data-stu-id="04cc9-105">Setting</span></span>

<span data-ttu-id="04cc9-106">A **ação StopMacro** não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="04cc9-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="04cc9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="04cc9-107">Remarks</span></span>

<span data-ttu-id="04cc9-108">Normalmente, você usa essa ação quando uma condição torna necessário parar a macro.</span><span class="sxs-lookup"><span data-stu-id="04cc9-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="04cc9-109">Você pode usar uma expressão condicional na linha de ação da macro, contendo essa ação.</span><span class="sxs-lookup"><span data-stu-id="04cc9-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="04cc9-110">Quando a expressão é avaliada como **True** (–1), o Microsoft Access interrompe a macro.</span><span class="sxs-lookup"><span data-stu-id="04cc9-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="04cc9-111">Por exemplo, você pode criar uma macro que abre um formulário mostrando os totais de ordem diária para a data inserida em uma caixa de diálogo personalizada.</span><span class="sxs-lookup"><span data-stu-id="04cc9-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="04cc9-112">Você pode usar uma expressão condicional para garantir que o controle **Data** do Pedido na caixa de diálogo contenha uma data válida.</span><span class="sxs-lookup"><span data-stu-id="04cc9-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="04cc9-113">Se isso não for o caso, a **ação MessageBox** poderá exibir uma mensagem de erro e a **ação PararMacro** poderá interromper a macro.</span><span class="sxs-lookup"><span data-stu-id="04cc9-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="04cc9-114">Se a macro tiver usado as ações **Eco** ou **DefinirAvisos** para desativar o eco ou a exibição de mensagens do sistema, a ação **PararMacro** as ativará automaticamente.</span><span class="sxs-lookup"><span data-stu-id="04cc9-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="04cc9-115">Esta ação não está disponível em um módulo VBA (Visual Basic for Applications).</span><span class="sxs-lookup"><span data-stu-id="04cc9-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="04cc9-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="04cc9-116">Example</span></span>

<span data-ttu-id="04cc9-117">A macro a seguir demonstra o uso da **ação AoOcorrer** Erro.</span><span class="sxs-lookup"><span data-stu-id="04cc9-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="04cc9-118">Neste exemplo, a ação **OnError** especifica que o Access execute uma macro de tratamento de erro personalizada chamada ErrorHandler quando ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="04cc9-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="04cc9-119">Quando ocorre um erro, o submacro CatchErrors é chamado.</span><span class="sxs-lookup"><span data-stu-id="04cc9-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="04cc9-120">Se o número do erro for 2102, uma mensagem específica será exibida e a execução da macro será interrompida.</span><span class="sxs-lookup"><span data-stu-id="04cc9-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="04cc9-121">Caso contrário, uma mensagem que descreve o erro será exibida e a macro será pausada para que você possa executar soluções de problemas adicionais.</span><span class="sxs-lookup"><span data-stu-id="04cc9-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="04cc9-122">A macro ErrorHandler exibe uma caixa de mensagem que se refere ao objeto **MacroError** para exibir informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="04cc9-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="04cc9-123">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="04cc9-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
