---
title: Ação de macro StopMacro
TOCTitle: StopMacro Macro Action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a918fd128456450c21b5a36e74b7266df661cb75
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463675"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="1c100-102">Ação de macro StopMacro</span><span class="sxs-lookup"><span data-stu-id="1c100-102">StopMacro Macro Action</span></span>

<span data-ttu-id="1c100-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c100-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c100-104">Você pode usar a ação **PararMacro** para interromper a macro em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="1c100-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="1c100-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="1c100-105">Setting</span></span>

<span data-ttu-id="1c100-106">A ação **PararMacro** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="1c100-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c100-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c100-107">Remarks</span></span>

<span data-ttu-id="1c100-108">Geralmente você usa esta ação quando uma condição torna necessário para interromper a macro.</span><span class="sxs-lookup"><span data-stu-id="1c100-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="1c100-109">Você pode usar uma expressão condicional na linha de ação da macro, contendo essa ação.</span><span class="sxs-lookup"><span data-stu-id="1c100-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="1c100-110">Quando a expressão for avaliada como **True** (– 1), o Microsoft Access interrompe a macro.</span><span class="sxs-lookup"><span data-stu-id="1c100-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="1c100-111">Por exemplo, você pode criar uma macro que abre um formulário mostrando os totais de ordem de diário para a data inserida em uma caixa de diálogo personalizada.</span><span class="sxs-lookup"><span data-stu-id="1c100-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="1c100-112">Você poderia usar uma expressão condicional para certificar-se de que o controle de **Data do pedido** na caixa de diálogo contém uma data válida.</span><span class="sxs-lookup"><span data-stu-id="1c100-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="1c100-113">Caso contrário, a ação **MessageBox** pode exibir uma mensagem de erro e a ação **PararMacro** pode interromper a macro.</span><span class="sxs-lookup"><span data-stu-id="1c100-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="1c100-114">Se a macro tiver usado as ações **eco** ou **DefinirAvisos** para desativar o eco ou a exibição de mensagens do sistema desativado, a ação **PararMacro** automaticamente os ativará.</span><span class="sxs-lookup"><span data-stu-id="1c100-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="1c100-115">Esta ação não está disponível em um módulo VBA (Visual Basic for Applications).</span><span class="sxs-lookup"><span data-stu-id="1c100-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="1c100-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1c100-116">Example</span></span>

<span data-ttu-id="1c100-117">A macro a seguir demonstra o uso da ação **AoOcorrerErro** .</span><span class="sxs-lookup"><span data-stu-id="1c100-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="1c100-118">Neste exemplo, a ação **AoOcorrerErro** Especifica que o Access executa um macro chamada Manipuladorerro quando ocorre um erro de tratamento de erros personalizado.</span><span class="sxs-lookup"><span data-stu-id="1c100-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="1c100-119">Quando ocorre um erro, submacro CatchErrors é chamado.</span><span class="sxs-lookup"><span data-stu-id="1c100-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="1c100-120">Se o número do erro for 2102, será exibida uma mensagem específica e execução da macro é interrompida.</span><span class="sxs-lookup"><span data-stu-id="1c100-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="1c100-121">Caso contrário, será exibida uma mensagem descrevendo o erro e a macro é pausada para que você possa realizar a solução de problemas adicionais.</span><span class="sxs-lookup"><span data-stu-id="1c100-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="1c100-122">A macro Manipuladorerro exibe uma caixa de mensagem que faz referência ao objeto **MacroError** para exibir informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="1c100-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="1c100-123">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="1c100-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
