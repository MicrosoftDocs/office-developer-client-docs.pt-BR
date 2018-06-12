---
title: Funções assíncronas definidas pelo usuário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5b64dfd4308da4efb5e94010fe1dc9d758a1199c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765247"
---
# <a name="asynchronous-user-defined-functions"></a>Funções assíncronas definidas pelo usuário

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 pode chamar funções definidas pelo usuário de forma assíncrona. Chamando funções de forma assíncrona pode melhorar o desempenho, permitindo que vários cálculos executar ao mesmo tempo. Quando você executar funções definidas pelo usuário em um cluster de computação, chamar funções de forma assíncrona permite que vários computadores a serem usadas para concluir os cálculos.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Quando usar funções assíncronas definidas pelo usuário

Algumas funções definidas pelo usuário devem aguardar por recursos externos. Enquanto aguardam, o thread de cálculo do Excel está bloqueado. No Excel 2013, funções definidas pelo usuário podem ser executado de maneira assíncrona. Isso libera o thread de cálculo para executar outros cálculos enquanto aguarda a função definida pelo usuário.
  
No Excel 2007, programadores pode executar várias funções definidas pelo usuário ao mesmo tempo, aumentando o número de threads usados no recálculos de vários threads. Esse método tem desvantagens, principalmente porque o número de threads é uma configuração com escopo para um aplicativo e não pode ser controlado no nível de uma única função ou um suplemento.
  
Programadores devem usar chamadas assíncronas de função definida pelo usuário quando a função deve esperar para recursos externos. Por exemplo, uma função que envia uma solicitação SOAP pela Internet deve aguardar a rede oferecer a solicitação, o servidor remoto para concluir a solicitação e a rede para retornar o resultado. Nesse caso, não há nenhuma ocorrência de computação significativa e Excel pode continuar com outros cálculos.
  
Programadores também podem usar as funções assíncronas definidas pelo usuário quando uma função está enviando solicitações para um cluster de computação. Nesse caso, não há apenas a latência de rede para aguardar, mas o cluster pode executar chamadas separadas em servidores separados. Por não aguardando para cada chamada finalizar, as chamadas podem ser sobrepostas para melhorar o desempenho. Em alguns casos, essa melhoria é significativa.
  
> [!NOTE]
> Funções definidas pelo usuário não podem ser registradas como ambos assíncrona e cluster seguras. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Gravar uma função de assíncrona definidas pelo usuário

Funções assíncronas definidas pelo usuário devem ficar atento a uma alça e use esse identificador quando informando que o Excel que a chamada de função está concluída. Uma função de assíncrona definidas pelo usuário é dividida em duas partes. A primeira delas é o ponto de entrada UDF standard, que iniciará uma operação assíncrona em segundo lugar, separada. Retornos de chamada para o Excel devem ser feitos durante o ponto de entrada do UDF. A primeira parte de inicialização da função retornarão o controle do seu thread de cálculo para o Excel, que continuará cálculo. Quando a operação assíncrona segunda estiver concluída, ela deve chamada de retorno no Excel e oferecer ao Excel seu resultado. 
  
> [!NOTE]
> Argumentos que são necessárias para a parte assíncrona passados para o UDF a função deve ser minuciosa copiado porque o Excel libera desses argumentos quando o ponto de entrada do UDF retorna. 
  
Excel fornece um conjunto de eventos que um suplemento XLL pode usar para gerenciar o ciclo de vida de chamadas UDF assíncronas. Esses eventos indicam que o Excel foi concluída com cálculos ou que o cálculo foi cancelado.
  
### <a name="declaring-an-asynchronous-function"></a>Declarando uma função assíncrona

Você deve declarar funções assíncronas definidas pelo usuário, como assíncrono quando eles são registrados. Isso é feito adicionando um parâmetro que aponta para uma estrutura XLOPER12, representado por um "X" na sequência de tipo de registro, em qualquer lugar na lista de parâmetros UDF. Excel usa esse parâmetro para passar o identificador da chamada assíncrona. O suplemento XLL deve passar o identificador da chamada assíncrona e o resultado da função para o Excel quando o resultado estiver pronto. Além disso, o tipo de retorno do UDF deve estar **void**, designados por ">" como o primeiro caractere na sequência de tipo. O tipo de retorno será considerada nulo porque a parte síncrona do UDF não retorna um valor para o Excel. Em vez disso, o suplemento XLL retorna um valor de maneira assíncrona por meio de um retorno de chamada. 
  
Você pode declarar funções assíncronas como thread-safe e, em seguida, a parte síncrona do UDF é usada em um recálculo multithread. 
  
O exemplo de código a seguir mostra uma função definida pelo usuário assíncrona registrada usando "\>QX" como a cadeia de caracteres de tipo de registro:
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Retornar valores

Quando o resultado da chamada assíncrona estiver pronto, o suplemento XLL retorna o resultado para o Excel, executando um retorno de chamada do tipo [xlAsyncReturn](xlasyncreturn.md).
  
**xlAsyncReturn** é o retorno de chamada só que pode ser usado em threads de não-cálculo durante o recálculo. Portanto, a parte assíncrona de uma UDF assíncrona não deve executar outros retornos de chamada. 
  
### <a name="handling-events"></a>Manipulando eventos

Iniciando no Excel 2010, XLLs podem receber eventos projetados para gerenciar o ciclo de vida de função assíncrona. Para obter mais informações, consulte [Manipulação de eventos](handling-events.md).
  
## <a name="see-also"></a>Confira também

- [Developing Excel XLLs](developing-excel-xlls.md)

