---
title: Funções assíncronas definidas pelo usuário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7fdf3bd09914981865c911fd65a78d044ad582f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412307"
---
# <a name="asynchronous-user-defined-functions"></a>Funções assíncronas definidas pelo usuário

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Microsoft Excel 2013 pode chamar funções definidas pelo usuário de forma assíncrona. Chamar funções de forma assíncrona pode melhorar o desempenho permitindo a execução de vários cálculos ao mesmo tempo. Quando executar funções definidas pelo usuário em um cluster de cálculo, chamando funções de forma assíncrona permite que vários computadores sejam usados para concluir os cálculos.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Quando usar funções assíncronas definidas pelo usuário

Algumas funções definidas pelo usuário devem aguardar recursos externos. Enquanto aguardam, o thread de cálculo do Excel é bloqueado. No Excel 2013, as funções definidas pelo usuário podem ser executados de forma assíncrona. Isso libera o thread de cálculo para executar outros cálculos enquanto a função definida pelo usuário aguarda.
  
No Excel 2007, os programadores podiam executar várias funções definidas pelo usuário ao mesmo tempo aumentando o número de threads usados em recálculações de vários threads. Esse método tem desvantagens principalmente porque o número de threads é uma configuração com escopo para um aplicativo e não pode ser controlada no nível de uma única função ou de um complemento.
  
Os programadores devem usar chamadas de função assíncronas definidas pelo usuário quando a função deve aguardar recursos externos. Por exemplo, uma função que envia uma solicitação SOAP pela Internet deve aguardar até que a rede entregue a solicitação, o servidor remoto para concluir a solicitação e a rede para retornar o resultado. Nesse caso, não há computação significativa ocorrendo e o Excel pode continuar com outros cálculos.
  
Os programadores também podem usar funções assíncronas definidas pelo usuário quando uma função está enviando solicitações para um cluster de computação. Nesse caso, não há apenas latência de rede a ser aguardada, mas o cluster pode executar chamadas separadas em servidores separados. Ao não aguardar a finalização de cada chamada, as chamadas podem ser sobre listadas para melhorar o desempenho. Em alguns casos, essa melhoria é significativa.
  
> [!NOTE]
> Funções definidas pelo usuário não podem ser registradas como assíncronas e seguras de cluster. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Escrevendo uma função assíncrona definida pelo usuário

As funções assíncronas definidas pelo usuário devem acompanhar um alça e usá-lo ao informar ao Excel que a chamada de função foi concluída. Uma função assíncrona definida pelo usuário é dividida em duas partes. A primeira parte é o ponto de entrada UDF padrão, que iniciará uma segunda operação assíncrona separada. Os retornos de chamada no Excel devem ser feitos durante o ponto de entrada UDF. A primeira parte de lançamento da função retornará o controle de seu thread de cálculo para o Excel, que continuará o cálculo. Quando a segunda operação assíncrona for concluída, ela deverá retornar ao Excel e fornecer o resultado ao Excel. 
  
> [!NOTE]
> Todos os argumentos passados para a UDF necessários para a parte assíncrona da função devem ser copiados em profundidade porque o Excel libera esses argumentos quando o ponto de entrada UDF retorna. 
  
O Excel fornece um conjunto de eventos que um complemento XLL pode usar para gerenciar o ciclo de vida de chamadas UDF assíncronas. Esses eventos indicam que o Excel terminou com cálculos ou que o cálculo foi cancelado.
  
### <a name="declaring-an-asynchronous-function"></a>Declarando uma função assíncrona

Você deve declarar funções assíncronas definidas pelo usuário como assíncronas quando elas são registradas. Isso é realizado adicionando-se um parâmetro que aponta para uma estrutura XLOPER12, representada por "X" na cadeia de caracteres de tipo de registro, em qualquer lugar na lista de parâmetros UDF. O Excel usa esse parâmetro para passar o alça de chamada assíncrona. O complemento XLL deve passar o alça de chamada assíncrona e o resultado da função de volta para o Excel quando o resultado estiver pronto. Além disso, o tipo de retorno da UDF deve ser **nulo,** designado por ">" como o primeiro caractere na cadeia de caracteres de tipo. O tipo de retorno é nulo porque a parte síncrona da UDF não retorna um valor para o Excel. Em vez disso, o complemento XLL retorna um valor de forma assíncrona por meio de um retorno de chamada. 
  
Você pode declarar funções assíncronas como thread-safe e, em seguida, a parte síncrona da UDF é usada em um recálculo multi-threaded. 
  
O exemplo de código a seguir mostra uma função assíncrona definida pelo usuário registrada usando " QX" como a cadeia de caracteres \> de tipo de registro:
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Retornando valores

Quando o resultado da chamada assíncrona estiver pronto, o complemento XLL retornará o resultado para o Excel executando um retorno de chamada do tipo [xlAsyncReturn](xlasyncreturn.md).
  
**xlAsyncReturn** é o único retorno de chamada que você pode usar em threads que não são de cálculo durante o recálculo. Portanto, a parte assíncrona de uma UDF assíncrona não deve executar nenhum outro retorno de chamada. 
  
### <a name="handling-events"></a>Manipular eventos

A partir do Excel 2010, XLLs podem receber eventos projetados para gerenciar o ciclo de vida da função assíncrona. Para obter mais informações, consulte [Manipulando eventos.](handling-events.md)
  
## <a name="see-also"></a>Confira também

- [Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

