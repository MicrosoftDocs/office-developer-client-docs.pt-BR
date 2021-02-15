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
# <a name="submacro-macro-statement"></a>Instrução de macro Submacro

**Aplica-se ao:** Access 2013, Office 2013

A **instrução Submacro** define uma macro separada na janela Designer de Macros.

## <a name="setting"></a>Setting

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
<td><p>Nome</p></td>
<td><p>Sim</p></td>
<td><p>Uma cadeia de caracteres que aparece como o nome da macro.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Exemplo

A macro a seguir demonstra o uso da **ação AoOcorrer** Erro. Neste exemplo, a ação **OnError** especifica que o Access execute uma macro de tratamento de erro personalizada chamada ErrorHandler quando ocorrer um erro. Quando ocorre um erro, o submacro CatchErrors é chamado. Se o número do erro for 2102, uma mensagem específica será exibida e a execução da macro será interrompida. Caso contrário, uma mensagem que descreve o erro será exibida e a macro será pausada para que você possa executar soluções de problemas adicionais. A macro ErrorHandler exibe uma caixa de mensagem que se refere ao objeto **MacroError** para exibir informações sobre o erro.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
