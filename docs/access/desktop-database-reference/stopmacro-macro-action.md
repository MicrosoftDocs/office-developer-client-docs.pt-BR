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
# <a name="stopmacro-macro-action"></a>Ação de macro StopMacro

**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **PararMacro** para interromper a macro em execução no momento.

## <a name="setting"></a>Configuração

A ação **PararMacro** não tem nenhum argumento.

## <a name="remarks"></a>Comentários

Geralmente você usa esta ação quando uma condição torna necessário para interromper a macro. Você pode usar uma expressão condicional na linha de ação da macro, contendo essa ação. Quando a expressão for avaliada como **True** (– 1), o Microsoft Access interrompe a macro.

Por exemplo, você pode criar uma macro que abre um formulário mostrando os totais de ordem de diário para a data inserida em uma caixa de diálogo personalizada. Você poderia usar uma expressão condicional para certificar-se de que o controle de **Data do pedido** na caixa de diálogo contém uma data válida. Caso contrário, a ação **MessageBox** pode exibir uma mensagem de erro e a ação **PararMacro** pode interromper a macro.

Se a macro tiver usado as ações **eco** ou **DefinirAvisos** para desativar o eco ou a exibição de mensagens do sistema desativado, a ação **PararMacro** automaticamente os ativará.

Esta ação não está disponível em um módulo VBA (Visual Basic for Applications).

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
