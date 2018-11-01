---
title: Instrução de macro Submacro
TOCTitle: Submacro Macro Statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de0d7066927e3a3cf034197c15f4330302801c0a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885924"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="0bdcc-102">Instrução de macro Submacro</span><span class="sxs-lookup"><span data-stu-id="0bdcc-102">Submacro Macro Statement</span></span>

<span data-ttu-id="0bdcc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0bdcc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0bdcc-104">A instrução **Submacro** define uma macro separada na janela do Designer de Macros.</span><span class="sxs-lookup"><span data-stu-id="0bdcc-104">The **Submacro** statement defines a seperate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="0bdcc-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="0bdcc-105">Setting</span></span>

<span data-ttu-id="0bdcc-106">A ação **Submacro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="0bdcc-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bdcc-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="0bdcc-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="0bdcc-108">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0bdcc-108">Required</span></span></p></th>
<th><p><span data-ttu-id="0bdcc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bdcc-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bdcc-110">Name</span><span class="sxs-lookup"><span data-stu-id="0bdcc-110">Name</span></span></p></td>
<td><p><span data-ttu-id="0bdcc-111">Sim</span><span class="sxs-lookup"><span data-stu-id="0bdcc-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="0bdcc-112">Uma cadeia de caracteres que aparece como o nome da macro.</span><span class="sxs-lookup"><span data-stu-id="0bdcc-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="0bdcc-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0bdcc-113">Example</span></span>

<span data-ttu-id="0bdcc-114">A macro a seguir demonstra o uso da ação **AoOcorrerErro** .</span><span class="sxs-lookup"><span data-stu-id="0bdcc-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="0bdcc-115">Neste exemplo, a ação **AoOcorrerErro** Especifica que o Access executa um macro chamada Manipuladorerro quando ocorre um erro de tratamento de erros personalizado.</span><span class="sxs-lookup"><span data-stu-id="0bdcc-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="0bdcc-116">Quando ocorre um erro, submacro CatchErrors é chamado.</span><span class="sxs-lookup"><span data-stu-id="0bdcc-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="0bdcc-117">Se o número do erro for 2102, será exibida uma mensagem específica e execução da macro é interrompida.</span><span class="sxs-lookup"><span data-stu-id="0bdcc-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="0bdcc-118">Caso contrário, será exibida uma mensagem descrevendo o erro e a macro é pausada para que você possa realizar a solução de problemas adicionais.</span><span class="sxs-lookup"><span data-stu-id="0bdcc-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="0bdcc-119">A macro Manipuladorerro exibe uma caixa de mensagem que faz referência ao objeto **MacroError** para exibir informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="0bdcc-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="0bdcc-120">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="0bdcc-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
