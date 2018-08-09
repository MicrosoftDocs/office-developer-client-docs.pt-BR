---
title: Estados, funções e comandos do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- estados [excel 2007], [Excel 2007] de comandos, funções de planilha [Excel 2007], funções de folha de macro [Excel 2007], Estados do Excel
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765294"
---
# <a name="excel-commands-functions-and-states"></a>Estados, funções e comandos do Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Microsoft Excel reconhece dois tipos de funcionalidade adicionada muito diferentes: as funções e comandos.
  
## <a name="commands"></a>Comandos

No Excel, comandos têm as seguintes características:
  
- Eles realizar ações da mesma forma que os usuários fazem.
    
- Eles podem fazer qualquer coisa que um usuário pode fazer (assunto para os limites da interface utilizados), como alterar as configurações do Excel, abertura, fechamento e editando documentos, iniciando recálculos e assim por diante.
    
- Eles podem ser configurados para ser chamados quando ocorrerem determinados eventos capturados.
    
- Eles podem exibir caixas de diálogo e interagir com o usuário.
    
- Eles podem ser vinculados para controlar objetos para que eles são chamados quando alguma ação seja executada nesse objeto, como o mouse.
    
- Eles nunca são chamados pelo Excel durante um recálculo.
    
- Eles não podem ser chamados pelas funções durante um recálculo.
    
## <a name="functions"></a>Funções

Funções do Excel faça o seguinte:
  
- Eles geralmente levam argumentos e sempre retornam um resultado.
    
- Eles podem ser inseridos em uma ou mais células como parte de uma fórmula do Excel.
    
- Eles podem ser usados em definições do nome definido.
    
- Eles podem ser usados em expressões de limite e de limite de formatação condicional.
    
- Eles podem ser chamados pelos comandos.
    
- Eles não é possível chamar comandos.
    
Excel faz outra distinção entre funções de planilha definidas pelo usuário e as funções definidas pelo usuário são projetadas para trabalhar em folhas de macro. Excel não limitam as funções de planilha de macro definida pelo usuário apenas a que está sendo usado em folhas de macro: essas funções podem ser usadas em qualquer lugar, uma função de planilha normal pode ser usada.
  
### <a name="worksheet-functions"></a>Funções de Planilha

O exemplo a seguir for verdadeira das funções de planilha do Excel:
  
- Eles não podem acessar as funções de informações de folha de macro.
    
- Eles não podem obter os valores das células não calculadas.
    
- Eles podem ser gravados e registrados como thread-safe iniciando no Excel 2007.
    
### <a name="macro-sheet-functions"></a>Funções de folha de macro

O exemplo a seguir for verdadeira das funções de folha de macro do Excel:
  
- Eles podem acessar as funções de informações de folha de macro.
    
- Eles podem obter os valores das células não calculadas, incluindo os valores das células da chamada.
    
- Eles não são considerados thread seguros iniciada no Excel 2007.
    
Como o Excel trata uma função definida pelo usuário (UDF), o que permite a função fazer e como ele recalcula a função são determinados tudo ao registrar a função. Se uma função está registrada como uma função de planilha, mas tenta fazer algo que apenas uma função de folha de macro pode fazer, a operação falhará. Iniciando no Excel 2007, se uma função de planilha registrada como thread-safe tenta chamar uma função de folha de macro, novamente, a operação falhará.
  
Excel trata do Microsoft Visual Basic for Applications (VBA) UDFs como funções equivalente a folha de macro, em que eles possam acessar informações de espaço de trabalho e o valor das células não calculadas e eles não são considerados como thread iniciando seguros no Excel 2007.
  
## <a name="excel-states"></a>Estados do Excel

Excel pode estar em um dos vários estados a qualquer momento determinado, dependendo das ações do usuário, um processo externo, um evento capturado executando uma macro ou um evento de manutenção do sistema do Excel cronometrado como **salvamento automático**.
  
Os estados de experiências de usuário são:
  
- **Estado está pronto:** Não há comandos ou macros estão sendo executadas. Sem caixas de diálogo estiver sendo exibidas. Nenhuma célula estiver sendo editada e o usuário não estiver no meio de uma operação de Recortar/copiar e colar. Nenhum objeto incorporado tem o foco. 
    
- **Modo de edição:** O usuário foi iniciada digitar caracteres válidos de entrada em uma célula desbloqueada ou desprotegida ou pressionou **F2** em uma ou mais células desbloqueadas ou desprotegidas. 
    
- **Modo Recortar/copiar e colar:** O usuário tem recortado ou copiado de uma célula ou intervalo de células e tem não ainda coladas-los ou tem colado-los usando a caixa de diálogo Colar especial, que permite que várias operações de colagem. 
    
- **Modo ponto:** O usuário está editando uma fórmula e está selecionando células cujos endereços são adicionados à fórmula está sendo editada. 
    
O usuário pode desmarcar a editar, ponto e modos de Recortar/copiar pressionando a tecla **ESC** , que retorna o Excel ao estado pronto. Outros eventos podem limpar desses estados, como o seguinte: 
  
- O usuário abre uma caixa de diálogo interna.
    
- O usuário inicia um recálculo.
    
- O usuário executa um comando.
    
- Excel executa uma operação de **salvamento automático** . 
    
- Um evento timer é interceptado.
    
O exemplo a último é de importância ao suplemento desenvolvedores. Você deve considerar o impacto da usabilidade normal do Excel em que intercepta o evento timer frequente estão sendo definidos e executadas. Quando isso é uma parte importante do funcionalidade da seu suplemento, você deve fornecer aos usuários uma maneira podem ser acessada facilmente de suspendendo, para que eles podem Recortar/copiar e colar, normalmente, quando eles precisam.
  
## <a name="see-also"></a>Confira também



[Excel Programming Concepts](excel-programming-concepts.md)
  
[Permitir intervenções de usuário em operações demoradas](permitting-user-breaks-in-lengthy-operations.md)

