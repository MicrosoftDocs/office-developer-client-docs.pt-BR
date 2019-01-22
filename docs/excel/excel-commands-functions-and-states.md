---
title: Estados, funções e comandos do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- estados [Excel 2007],comandos [Excel 2007],funções de planilha [Excel 2007],funções de planilha de macro [Excel 2007],estados do Excel
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716233"
---
# <a name="excel-commands-functions-and-states"></a>Estados, funções e comandos do Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Microsoft Excel reconhece dois tipos bem distintos de funcionalidade adicionada: comandos e funções.
  
## <a name="commands"></a>Comandos

No Excel, os comandos têm as seguintes características:
  
- Realizam ações da mesma forma que os usuários.
    
- Podem realizar as mesmas ações que um usuário (sujeito aos limites da interface usada), como alterar as configurações do Excel, abrir, fechar e editar documentos, iniciar recálculos e muito mais.
    
- Podem ser configurados para ser chamados quando certos eventos interceptados ocorrerem.
    
- Podem exibir caixas de diálogo e interagir com o usuário.
    
- Podem ser vinculados a objetos de controle para que sejam chamados quando alguma ação for executada nesse objeto, como clicar com o botão esquerdo do mouse.
    
- Nunca são chamados pelo Excel durante um recálculo.
    
- Não podem ser chamados pela funções durante o recálculo.
    
## <a name="functions"></a>Funções

As ações no Excel realizam o seguinte:
  
- Geralmente usam argumentos e sempre retornam um resultado.
    
- Podem ser inseridas em uma ou mais células como parte de uma fórmula do Excel.
    
- Podem ser usadas em definições de nome definido.
    
- Podem ser usadas ​​em expressões de limite e limite de formatação condicional.
    
- Podem ser chamadas pelos comandos.
    
- Não podem chamar comandos.
    
O Excel faz uma distinção adicional entre funções de planilha definidas pelo usuário e funções definidas pelo usuário que são projetadas para trabalhar em planilhas de macro. O Excel não limita as funções de planilha de macro definidas pelo usuário somente para uso em planilhas de macro: essas funções podem ser usadas em qualquer lugar que uma função de planilha normal pode ser usada.
  
### <a name="worksheet-functions"></a>Funções de planilha

As seguintes condições são verdadeiras para as funções de planilha do Excel:
  
- Não podem acessar as funções de informação de planilha de macro.
    
- Não podem obter os valores de células não calculadas.
    
- Podem ser criadas e registradas como thread-safe, começando no Excel 2007.
    
### <a name="macro-sheet-functions"></a>Funções de planilha de macro

As seguintes condições são verdadeiras para as funções de planilha de macro do Excel:
  
- Podem acessar as funções de informação de planilha de macro.
    
- Podem obter os valores de células não calculadas, inclusive os valores das células chamadas.
    
- Não são consideradas thread-safe, começando no Excel 2007.
    
Quando você registra a função, determina como o Excel trata uma UDF (função definida pelo usuário), o que permite que a função faça e como ela recalcula a função. Se uma função for registrada como uma função de planilha, mas tenta fazer algo que somente uma função de planilha de macro pode fazer, a operação falhará. Desde o Excel 2007, se uma função de planilha registrada como thread-safe tentar chamar uma função de planilha de macro, novamente, a operação falhará.
  
O Excel trata as UDFs do VBA (Microsoft Visual Basic for Applications) como funções equivalentes a planilhas de macro, pois elas podem acessar informações de espaço de trabalho e o valor de células não calculadas, e não são consideradas como thread-safe desde o Excel 2007.
  
## <a name="excel-states"></a>Estados do Excel

O Excel pode estar em um dos vários estados a qualquer momento, dependendo das ações do usuário, de um processo externo, de um evento interceptado executando uma macro ou de um evento de manutenção do Excel, como **Salvamento Automático**.
  
Os estados experimentados pelo usuário são os seguintes:
  
- **Estado Pronto:** nenhum comando ou macro está sendo executado. Nenhuma caixa de diálogo está sendo exibida. Nenhuma célula está sendo editada e o usuário não está no meio de uma operação de recortar/copiar e colar. Nenhum objeto inserido está focado. 
    
- **Modo Editar:** o usuário começou a digitar caracteres de entrada válidos em uma célula desbloqueada ou desprotegida, ou pressionou **F2** em uma ou mais células desbloqueadas ou desprotegidas. 
    
- **Modo Recortar/copiar e colar:** o usuário recortou ou copiou uma célula ou um intervalo de células e ainda não colou, ou colou usando a caixa de diálogo especial de colagem, que permite várias operações de colagem. 
    
- **Modo Apontar:** o usuário está editando uma fórmula e selecionando células cujos endereços são adicionados à fórmula que está sendo editada. 
    
O usuário pode limpar os modos Editar, Apontar e Recortar/copiar pressionando a tecla **ESC**, que retorna o Excel ao estado pronto. Outros eventos podem limpar esses estados, como: 
  
- O usuário abre uma caixa de diálogo interna.
    
- O usuário inicia um recálculo.
    
- O usuário executa um comando.
    
- O Excel executa uma operação de **Salvamento Automático**. 
    
- Um evento de temporizador é interceptado.
    
O último exemplo é importante para os desenvolvedores de suplementos. Você deve considerar o impacto da usabilidade normal do Excel, em que as interceptações de eventos de temporizador frequentes estão sendo definidas e executadas. Quando essa for uma parte importante da funcionalidade de seu suplemento, ofereça aos usuários uma forma facilmente acessível de suspendê-la, para que eles possam recortar/copiar e colar normalmente quando precisarem.
  
## <a name="see-also"></a>Confira também



[Conceitos de programação do Excel](excel-programming-concepts.md)
  
[Permitir intervenções de usuário em operações demoradas](permitting-user-breaks-in-lengthy-operations.md)

