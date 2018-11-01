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
# <a name="submacro-macro-statement"></a>Instrução de macro Submacro

**Aplica-se a**: Access 2013, o Office 2013

A instrução **Submacro** define uma macro separada na janela do Designer de Macros.

## <a name="setting"></a>Configuração

A ação **Submacro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Sim</p></td>
<td><p>Uma cadeia de caracteres que aparece como o nome da macro.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Exemplo

A macro a seguir demonstra o uso da ação **AoOcorrerErro** . Neste exemplo, a ação **AoOcorrerErro** Especifica que o Access executa um macro chamada Manipuladorerro quando ocorre um erro de tratamento de erros personalizado. Quando ocorre um erro, submacro CatchErrors é chamado. Se o número do erro for 2102, será exibida uma mensagem específica e execução da macro é interrompida. Caso contrário, será exibida uma mensagem descrevendo o erro e a macro é pausada para que você possa realizar a solução de problemas adicionais. A macro Manipuladorerro exibe uma caixa de mensagem que faz referência ao objeto **MacroError** para exibir informações sobre o erro.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
