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
# <a name="onerror-macro-action"></a>Ação de macro AoOcorrerErro

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **AoOcorrerErro** para especificar o que deve acontecer quando ocorre um erro em uma macro.

## <a name="setting"></a>Configuração

A ação **AoOcorrerErro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Ir para</p></td>
<td><p>Especifique como deve ser o comportamento geral quando for encontrado um erro. Clique na seta suspensa e clique em uma das configurações a seguir:</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuração</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Next</strong></p></td>
<td><p>O Microsoft Office Access 2007 registra os detalhes do erro no objeto <strong>MacroError</strong>, mas não interrompe a macro. A macro continua com a ação seguinte.</p></td>
</tr>
<tr class="even">
<td><p><strong>Macro Name</strong></p></td>
<td><p>O Access interrompe a macro atual e executa aquela nomeada no argumento <strong>Nome da Macro</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Fail</strong></p></td>
<td><p>O Access para a macro atual e exibe uma mensagem de erro.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>Nome da Macro</p></td>
<td><p>Se o argumento ir para for definido como o nome da Macro, digite o nome da macro a ser usada para tratamento de erros. O nome que você digitar deve corresponder a um nome na coluna <strong>Nome da Macro</strong> da macro atual; Você não pode inserir o nome de um objeto de macro diferente. No exemplo a seguir, a macro <strong>Manipuladorerro</strong> está contida no mesmo objeto macro como a ação <strong>AoOcorrerErro</strong> . Este argumento precisará ficar em branco se o argumento ir para for definido como <strong>próximo</strong> ou <strong>falhar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

- A ação **AoOcorrerErro** normalmente é colocada no início de uma macro, mas você também pode colocar a ação na macro posteriormente. As regras estabelecidas pela ação entrarão em vigor sempre que a ação for executada.

- Se você definir o argumento Ir para como **Falhar**, o Access terá o mesmo comportamento de se não houvesse nenhuma ação **AoOcorrerErro** na macro. Isso significa que, se for encontrado um erro, o Access interromperá a macro e exibirá uma mensagem de erro padrão. O principal uso da configuração **Falhar** é desligar qualquer tratamento de erros que você tenha estabelecido anteriormente em uma macro.

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
