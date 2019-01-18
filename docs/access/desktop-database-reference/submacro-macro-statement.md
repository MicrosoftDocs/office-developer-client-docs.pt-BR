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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716191"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="c43ab-102">Instrução de macro Submacro</span><span class="sxs-lookup"><span data-stu-id="c43ab-102">Submacro macro statement</span></span>

<span data-ttu-id="c43ab-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c43ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c43ab-104">A instrução **Submacro** define uma macro separada na janela do Designer de macros.</span><span class="sxs-lookup"><span data-stu-id="c43ab-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="c43ab-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="c43ab-105">Setting</span></span>

<span data-ttu-id="c43ab-106">A ação **Submacro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c43ab-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c43ab-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="c43ab-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="c43ab-108">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c43ab-108">Required</span></span></p></th>
<th><p><span data-ttu-id="c43ab-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c43ab-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c43ab-110">Name</span><span class="sxs-lookup"><span data-stu-id="c43ab-110">Name</span></span></p></td>
<td><p><span data-ttu-id="c43ab-111">Sim</span><span class="sxs-lookup"><span data-stu-id="c43ab-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="c43ab-112">Uma cadeia de caracteres que aparece como o nome da macro.</span><span class="sxs-lookup"><span data-stu-id="c43ab-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="c43ab-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c43ab-113">Example</span></span>

<span data-ttu-id="c43ab-114">A macro a seguir demonstra o uso da ação **AoOcorrerErro** .</span><span class="sxs-lookup"><span data-stu-id="c43ab-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="c43ab-115">Neste exemplo, a ação **AoOcorrerErro** Especifica que o Access executa um macro chamada Manipuladorerro quando ocorre um erro de tratamento de erros personalizado.</span><span class="sxs-lookup"><span data-stu-id="c43ab-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="c43ab-116">Quando ocorre um erro, submacro CatchErrors é chamado.</span><span class="sxs-lookup"><span data-stu-id="c43ab-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="c43ab-117">Se o número do erro for 2102, será exibida uma mensagem específica e execução da macro é interrompida.</span><span class="sxs-lookup"><span data-stu-id="c43ab-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="c43ab-118">Caso contrário, será exibida uma mensagem descrevendo o erro e a macro é pausada para que você possa realizar a solução de problemas adicionais.</span><span class="sxs-lookup"><span data-stu-id="c43ab-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="c43ab-119">A macro Manipuladorerro exibe uma caixa de mensagem que faz referência ao objeto **MacroError** para exibir informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="c43ab-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="c43ab-120">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c43ab-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
