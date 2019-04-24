---
title: Ação da macro PararMacro
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308495"
---
# <a name="stopmacro-macro-action"></a>Ação da macro PararMacro

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **PararMacro** para interromper a macro em execução no momento.

## <a name="setting"></a>Configuração

A ação **PararMacro** não tem argumentos.

## <a name="remarks"></a>Comentários

Normalmente, você usa esta ação quando uma condição torna necessário parar a macro. Você pode usar uma expressão condicional na linha de ação da macro, contendo essa ação. Quando a expressão é avaliada como **true** (– 1), o Microsoft Access interrompe a macro.

Por exemplo, você pode criar uma macro que abre um formulário mostrando os totais de pedidos diários da data inserida em uma caixa de diálogo personalizada. Você pode usar uma expressão condicional para ter certeza de que o controle de **data da ordem** na caixa de diálogo contém uma data válida. Caso contrário, a ação **MessageBox** poderá exibir uma mensagem de erro e a ação **PararMacro** poderá interromper a macro.

Se a macro tiver usado as ações **eco** ou SetWarnings para ativar o eco ou a exibição de mensagens do sistema, a ação **PararMacro** as ativará automaticamente. ****

Esta ação não está disponível em um módulo VBA (Visual Basic for Applications).

## <a name="example"></a>Exemplo

A macro a seguir demonstra o uso da ação **AoOcorrerErro** . Neste exemplo, a ação **AoOcorrerErro** especifica que o Access executa uma macro de tratamento de erros personalizada chamada ErrorHandler quando ocorre um erro. Quando ocorre um erro, a submacro CatchErrors é chamada. Se o número de erro for 2102, uma mensagem específica é exibida e a execução da macro é interrompida. Caso contrário, uma mensagem descrevendo o erro é exibida e a macro é pausada para que você possa executar a solução de problemas adicional. A macro ErrorHandler exibe uma caixa de mensagem que se refere ao objeto **MacroError** para exibir informações sobre o erro.

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
