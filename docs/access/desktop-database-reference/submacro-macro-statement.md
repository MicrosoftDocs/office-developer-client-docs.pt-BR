---
title: Instrução de macro Submacro
TOCTitle: Submacro macro statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caabfb0f4e90134c10d5ab728f19e1fd2a4437dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308467"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="e6875-102">Instrução de macro Submacro</span><span class="sxs-lookup"><span data-stu-id="e6875-102">Submacro macro statement</span></span>

<span data-ttu-id="e6875-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6875-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6875-104">A \*\*\*\* instrução submacro define uma macro separada na janela do designer de macros.</span><span class="sxs-lookup"><span data-stu-id="e6875-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="e6875-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="e6875-105">Setting</span></span>

<span data-ttu-id="e6875-106">A ação **Submacro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e6875-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6875-107">Argument</span><span class="sxs-lookup"><span data-stu-id="e6875-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="e6875-108">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e6875-108">Required</span></span></p></th>
<th><p><span data-ttu-id="e6875-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6875-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6875-110">Nome</span><span class="sxs-lookup"><span data-stu-id="e6875-110">Name</span></span></p></td>
<td><p><span data-ttu-id="e6875-111">Sim</span><span class="sxs-lookup"><span data-stu-id="e6875-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="e6875-112">Uma cadeia de caracteres que aparece como o nome da macro.</span><span class="sxs-lookup"><span data-stu-id="e6875-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="e6875-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e6875-113">Example</span></span>

<span data-ttu-id="e6875-114">A macro a seguir demonstra o uso da ação **AoOcorrerErro** .</span><span class="sxs-lookup"><span data-stu-id="e6875-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="e6875-115">Neste exemplo, a ação **AoOcorrerErro** especifica que o Access executa uma macro de tratamento de erros personalizada chamada ErrorHandler quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="e6875-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="e6875-116">Quando ocorre um erro, a submacro CatchErrors é chamada.</span><span class="sxs-lookup"><span data-stu-id="e6875-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="e6875-117">Se o número de erro for 2102, uma mensagem específica é exibida e a execução da macro é interrompida.</span><span class="sxs-lookup"><span data-stu-id="e6875-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="e6875-118">Caso contrário, uma mensagem descrevendo o erro é exibida e a macro é pausada para que você possa executar a solução de problemas adicional.</span><span class="sxs-lookup"><span data-stu-id="e6875-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="e6875-119">A macro ErrorHandler exibe uma caixa de mensagem que se refere ao objeto **MacroError** para exibir informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="e6875-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="e6875-120">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e6875-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
