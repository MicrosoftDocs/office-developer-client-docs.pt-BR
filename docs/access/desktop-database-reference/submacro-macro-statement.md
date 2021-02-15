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
# <a name="submacro-macro-statement"></a><span data-ttu-id="eba9c-102">Instrução de macro Submacro</span><span class="sxs-lookup"><span data-stu-id="eba9c-102">Submacro macro statement</span></span>

<span data-ttu-id="eba9c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eba9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eba9c-104">A **instrução Submacro** define uma macro separada na janela Designer de Macros.</span><span class="sxs-lookup"><span data-stu-id="eba9c-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="eba9c-105">Setting</span><span class="sxs-lookup"><span data-stu-id="eba9c-105">Setting</span></span>

<span data-ttu-id="eba9c-106">A ação **Submacro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="eba9c-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eba9c-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="eba9c-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="eba9c-108">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="eba9c-108">Required</span></span></p></th>
<th><p><span data-ttu-id="eba9c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="eba9c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eba9c-110">Nome</span><span class="sxs-lookup"><span data-stu-id="eba9c-110">Name</span></span></p></td>
<td><p><span data-ttu-id="eba9c-111">Sim</span><span class="sxs-lookup"><span data-stu-id="eba9c-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="eba9c-112">Uma cadeia de caracteres que aparece como o nome da macro.</span><span class="sxs-lookup"><span data-stu-id="eba9c-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="eba9c-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="eba9c-113">Example</span></span>

<span data-ttu-id="eba9c-114">A macro a seguir demonstra o uso da **ação AoOcorrer** Erro.</span><span class="sxs-lookup"><span data-stu-id="eba9c-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="eba9c-115">Neste exemplo, a ação **OnError** especifica que o Access execute uma macro de tratamento de erro personalizada chamada ErrorHandler quando ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="eba9c-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="eba9c-116">Quando ocorre um erro, o submacro CatchErrors é chamado.</span><span class="sxs-lookup"><span data-stu-id="eba9c-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="eba9c-117">Se o número do erro for 2102, uma mensagem específica será exibida e a execução da macro será interrompida.</span><span class="sxs-lookup"><span data-stu-id="eba9c-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="eba9c-118">Caso contrário, uma mensagem que descreve o erro será exibida e a macro será pausada para que você possa executar soluções de problemas adicionais.</span><span class="sxs-lookup"><span data-stu-id="eba9c-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="eba9c-119">A macro ErrorHandler exibe uma caixa de mensagem que se refere ao objeto **MacroError** para exibir informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="eba9c-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="eba9c-120">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="eba9c-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
