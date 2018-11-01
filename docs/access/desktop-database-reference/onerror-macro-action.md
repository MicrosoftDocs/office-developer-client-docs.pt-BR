---
title: Ação de macro AoOcorrerErro
TOCTitle: OnError Macro Action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e755683b4c040b37f0da12f7e67e8c400e62edb4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882137"
---
# <a name="onerror-macro-action"></a><span data-ttu-id="50462-102">Ação de macro AoOcorrerErro</span><span class="sxs-lookup"><span data-stu-id="50462-102">OnError Macro Action</span></span>

<span data-ttu-id="50462-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="50462-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50462-104">Você pode usar a ação **AoOcorrerErro** para especificar o que deve acontecer quando ocorre um erro em uma macro.</span><span class="sxs-lookup"><span data-stu-id="50462-104">You can use the **OnError** action to specify what should happen when an error occurs in a macro.</span></span>

## <a name="setting"></a><span data-ttu-id="50462-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="50462-105">Setting</span></span>

<span data-ttu-id="50462-106">A ação **AoOcorrerErro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="50462-106">The **OnError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50462-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="50462-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="50462-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="50462-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50462-109">Ir para</span><span class="sxs-lookup"><span data-stu-id="50462-109">Go to</span></span></p></td>
<td><p><span data-ttu-id="50462-p101">Especifique como deve ser o comportamento geral quando for encontrado um erro. Clique na seta suspensa e clique em uma das configurações a seguir:</span><span class="sxs-lookup"><span data-stu-id="50462-p101">Specify the general behavior that should occur when an error is encountered. Click the drop-down arrow and then click one of the following settings:</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50462-112">Configuração</span><span class="sxs-lookup"><span data-stu-id="50462-112">Setting</span></span></p></th>
<th><p><span data-ttu-id="50462-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="50462-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50462-114"><strong>Next</strong></span><span class="sxs-lookup"><span data-stu-id="50462-114"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="50462-p102">O Microsoft Office Access 2007 registra os detalhes do erro no objeto <strong>MacroError</strong>, mas não interrompe a macro. A macro continua com a ação seguinte.</span><span class="sxs-lookup"><span data-stu-id="50462-p102">Microsoft Office Access 2007 records the details of the error in the <strong>MacroError</strong> object but does not stop the macro. The macro continues with the next action.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50462-117"><strong>Macro Name</strong></span><span class="sxs-lookup"><span data-stu-id="50462-117"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="50462-118">O Access interrompe a macro atual e executa aquela nomeada no argumento <strong>Nome da Macro</strong>.</span><span class="sxs-lookup"><span data-stu-id="50462-118">Access stops the current macro and runs the macro that is named in the <strong>Macro Name</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50462-119"><strong>Fail</strong></span><span class="sxs-lookup"><span data-stu-id="50462-119"><strong>Fail</strong></span></span></p></td>
<td><p><span data-ttu-id="50462-120">O Access para a macro atual e exibe uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="50462-120">Access stops the current macro and displays an error message.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50462-121">Nome da Macro</span><span class="sxs-lookup"><span data-stu-id="50462-121">Macro Name</span></span></p></td>
<td><p><span data-ttu-id="50462-122">Se o argumento ir para for definido como o nome da Macro, digite o nome da macro a ser usada para tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="50462-122">If the Go to argument is set to Macro Name, type the name of the macro to be used for error handling.</span></span> <span data-ttu-id="50462-123">O nome que você digitar deve corresponder a um nome na coluna <strong>Nome da Macro</strong> da macro atual; Você não pode inserir o nome de um objeto de macro diferente.</span><span class="sxs-lookup"><span data-stu-id="50462-123">The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object.</span></span> <span data-ttu-id="50462-124">No exemplo a seguir, a macro <strong>Manipuladorerro</strong> está contida no mesmo objeto macro como a ação <strong>AoOcorrerErro</strong> .</span><span class="sxs-lookup"><span data-stu-id="50462-124">In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action.</span></span> <span data-ttu-id="50462-125">Este argumento precisará ficar em branco se o argumento ir para for definido como <strong>próximo</strong> ou <strong>falhar</strong>.</span><span class="sxs-lookup"><span data-stu-id="50462-125">This argument must be left blank if the Go to argument is set to <strong>Next</strong> or <strong>Fail</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="50462-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="50462-126">Remarks</span></span>

- <span data-ttu-id="50462-p104">A ação **AoOcorrerErro** normalmente é colocada no início de uma macro, mas você também pode colocar a ação na macro posteriormente. As regras estabelecidas pela ação entrarão em vigor sempre que a ação for executada.</span><span class="sxs-lookup"><span data-stu-id="50462-p104">The **OnError** action is usually placed at the beginning of a macro, but you can also place the action later in the macro. The rules established by the action will take effect whenever the action is run.</span></span>

- <span data-ttu-id="50462-p105">Se você definir o argumento Ir para como **Falhar**, o Access terá o mesmo comportamento de se não houvesse nenhuma ação **AoOcorrerErro** na macro. Isso significa que, se for encontrado um erro, o Access interromperá a macro e exibirá uma mensagem de erro padrão. O principal uso da configuração **Falhar** é desligar qualquer tratamento de erros que você tenha estabelecido anteriormente em uma macro.</span><span class="sxs-lookup"><span data-stu-id="50462-p105">If you set the Go to argument to **Fail**, Access behaves the same way it would if there were no **OnError** action in the macro. That is, if an error is encountered, Access stops the macro and displays a standard error message. The main use for the **Fail** setting is to turn off any error handling that you established earlier in a macro.</span></span>

## <a name="example"></a><span data-ttu-id="50462-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="50462-132">Example</span></span>

<span data-ttu-id="50462-133">A macro a seguir demonstra o uso da ação **AoOcorrerErro** .</span><span class="sxs-lookup"><span data-stu-id="50462-133">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="50462-134">Neste exemplo, a ação **AoOcorrerErro** Especifica que o Access executa um macro chamada Manipuladorerro quando ocorre um erro de tratamento de erros personalizado.</span><span class="sxs-lookup"><span data-stu-id="50462-134">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="50462-135">Quando ocorre um erro, submacro CatchErrors é chamado.</span><span class="sxs-lookup"><span data-stu-id="50462-135">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="50462-136">Se o número do erro for 2102, será exibida uma mensagem específica e execução da macro é interrompida.</span><span class="sxs-lookup"><span data-stu-id="50462-136">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="50462-137">Caso contrário, será exibida uma mensagem descrevendo o erro e a macro é pausada para que você possa realizar a solução de problemas adicionais.</span><span class="sxs-lookup"><span data-stu-id="50462-137">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="50462-138">A macro Manipuladorerro exibe uma caixa de mensagem que faz referência ao objeto **MacroError** para exibir informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="50462-138">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="50462-139">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="50462-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
