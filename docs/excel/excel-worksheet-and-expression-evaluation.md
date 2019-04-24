---
title: Planilha do Excel e avaliação de expressões
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- expressão de avaliação [Excel 2007], erros em planilhas [Excel 2007], cadeias de caracteres Unicode longas [Excel 2007], avaliando expressões [Excel 2007], avaliando planilhas [Excel 2007], avaliação de planilha [Excel 2007], erros de planilha [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cf1e0539136435f7d7df6ef348fc92ec4380e132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310980"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Planilha do Excel e avaliação de expressões

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O conteúdo da célula da planilha do Microsoft Excel é avaliado em um dos quatro tipos de dados básicos:
  
- **Números**
    
- **Booliano true** ou **false**
    
- **Cadeias de caracteres**
    
- **Erros**
    
Matrizes de tipo misto desses tipos também podem ser inseridas em fórmulas como argumentos para funções ou como valores que abrangem mais de uma célula em uma fórmula de matriz.
  
Quando um usuário (ou uma macro de comando) insere algo em uma célula, o Excel tenta interpretar a entrada e exibe uma mensagem de erro, caso não possa. Se a entrada começar com um prefixo de cadeia de caracteres (uma aspa simples), o Excel colocará todos os caracteres de entrada na célula conforme fornecido, sem modificações. (O prefixo da cadeia de caracteres não é exibido.) Se a entrada começar com **=**, **+**, ou **-**, o Excel tentará interpretar a entrada como uma fórmula. Se a sintaxe estiver incorreta ou se a avaliação for interrompida, um erro será exibido e a célula será colocada no modo de edição. Caso contrário, o Excel tentará identificar, converter e avaliar operadores e nomes de função e seus argumentos. 
  
Os operandos são avaliados da esquerda para a direita antes de o operador ser aplicado. As funções são avaliadas começando com os operadores de precedência mais alta e mais internos (mais aninhados). Se os argumentos de função ou operandos não puderem ser convertidos para os tipos esperados, a avaliação falhará e resultará em um **#VALUE!** #NUM! Quando um token (que não é um valor literal) não é reconhecido como uma função ou um nome ou rótulo definido, a avaliação falha e resulta em um **#NAME?** erro. 
  
Se a entrada não iniciar com nenhuma dessas coisas, o Excel verificará em relação a padrões conhecidos de entrada como datas, horas, valores monetários, porcentagens ou números e será interpretado de acordo. Isso é feito de uma maneira específica da localidade. Se nenhuma dessas interpretações fizer sentido, o Excel reverterá para considerar a entrada como uma cadeia de caracteres e a colocará na célula inalterada.
  
O Excel oferece suporte a outros tipos de dados, o que é uma referência de intervalo. O Excel converte as referências para os valores das células referenciadas ao avaliar argumentos de operadores e funções que não têm argumentos de referência, ou quando a expressão em uma fórmula de célula é reduzida para uma referência.
  
O Excel expõe a capacidade de reduzir qualquer cadeia de caracteres válida para um dos quatro tipos de dados de planilha básicos com a função XLM **avaliar** e seu equivalente de API de C **xlfEvaluate**. Essa função fornece, entre outras coisas, uma maneira simples de avaliar intervalos nomeados no código de DLL. Essa função difere do comportamento descrito anteriormente apenas, em vez de exibir mensagens de erro ou habilitar a edição de célula, ela retorna um **#VALUE!** erro se a expressão de avaliação falhar. 
  
## <a name="numbers"></a>Números

Todos os números de planilha do Excel são representados internamente como ponto flutuante de precisão dupla de 8 bytes, incluindo todos os números inteiros. No enTanto, a implementação desses números no Excel não é totalmente compatível com IEEE, conforme mostrado na tabela a seguir.
  
|**Tipo**|**Maximum**|**Mínimo**|
|:-----|:-----|:-----|
|IEEE de 8 bytes duplo  <br/> |1.7976931348623157 E + 308  <br/> |2.2250738585072014 E-308  <br/> |
|Planilha (retornada por função ou colar valor)  <br/> |1.7976931348623157 E + 308  <br/> |2.22507385850721 E-308  <br/> |
|Planilha (entrada manual)  <br/> |9.99999999999999 E + 307  <br/> |2.22507385850721 E-308  <br/> |
   
Os números IEEE normais (ou seja, números no intervalo 2.2250738585072009 E-308 a 4.9406564584124654 E-324) não são suportados em planilhas do Excel, mas têm suporte de duplicatas do VBA.
  
Se uma função de DLL retornar IEEE +/-Infinity ou um Double inválido, o Excel a converterá em **#NUM!**. Todos os números e números menores do que o mínimo positivo normal no Excel são convertidos em zero positivo. O IEEE negativo nulo tem suporte, ou seja, pode ser retornado por uma função de DLL e é exibido como **-0**. (O **\<** operador não verifica se há zero negativo e, portanto, **=\<a1 0** avalia como **true** se o a1 contiver zero negativo). 
  
Observe que determinados formatos de número têm limites mais estreitos que, por exemplo, datas e horas. A divisão de inteiros é, na verdade, a divisão de ponto flutuante e, em casos extremos, gera um resultado não inteiro onde o resultado preciso deve ser um inteiro.
  
## <a name="long-unicode-strings"></a>Cadeias de caracteres Unicode longas

Todas as cadeias de caracteres que o usuário vê no Excel têm muitas versões agora armazenadas internamente como cadeias de caracteres Unicode. As cadeias de caracteres de planilha Unicode podem ter até 32.767 (2<sup>15</sup> -1) em comprimento e podem conter qualquer caractere Unicode válido. 
  
Quando a API C foi introduzida pela primeira vez, as cadeias de caracteres da planilha eram limitadas de tamanho a 255 caracteres, e a API C reflete essas limitações. Com o Excel 2007, a API de C é atualizada para lidar com as cadeias de caracteres Unicode longas do Excel. Isso significa que as funções de DLL registradas da maneira certa podem aceitar argumentos Unicode e retornar cadeias de caracteres Unicode.
  
> [!NOTE]
> As cadeias de caracteres de byte ainda são totalmente compatíveis com a API C para compatibilidade com versões anteriores; no entanto, eles ainda têm o mesmo limite de 255 caracteres. 
  
## <a name="returning-errors"></a>Retornando erros

O Excel avalia as células para erros onde não pode converter os argumentos Function ou Operator para o tipo correto ou se ele não reconhece uma função ou um nome definido. Ambos os cenários foram descritos anteriormente. Quando as funções e operadores de planilha internas falham, elas também resultam em erros que informam o usuário sobre o tipo de falha. Você deve ter suas próprias funções de suplemento retornar erros que são consistentes com o comportamento no Excel.
  
### <a name="null"></a>#NULL!

O **#NULL!** o erro é retornado por algumas funções de informações de XLM. Por exemplo, chamar **Get. DOCUMENTO (78)** ou a função da API C equivalente **xlfGetDocument** com o argumento 78, quando não há impressoras instaladas resulta no retorno desse erro. Ele também pode ser retornado por algumas funções quando, por exemplo, avaliam uma cadeia de caracteres vazia. 
  
Você pode querer retornar esse erro da função do suplemento quando nenhum dos outros erros parecer apropriado.
  
### <a name="div0"></a>#DIV/0!

O operador de divisão do Excel retorna a **#DIV/0!** erro quando o denominador é avaliado como zero ou um número é muito pequeno para ser representado como não zero pelo Excel. Algumas funções que por definição envolvem uma divisão também podem retornar esse erro. Por exemplo, **média** retorna esse erro se nenhuma das entradas puder ser convertida para números. 
  
Você deve considerar apenas o retorno desse erro da função de suplemento para indicar que uma divisão por zero foi detectada.
  
### <a name="value"></a>#VALUE!

O Excel retorna a **#VALUE!** erro se um argumento Function ou Operator não pode ser convertido para o tipo necessário. No caso de argumentos de função que não podem ser convertidos, `=LN("X")`por exemplo, o Excel não chama o código de função. Esse é um ponto importante a ser lembrado ao escrever e depurar suas próprias funções de suplemento. 
  
Algumas funções retornam esse erro se um argumento não puder ser convertido dentro do código de função. Por exemplo, `DATEVALUE("30-Feb-2007")` falha com esse erro, apesar do argumento ser do tipo correto. Nesse caso, é a função que está retornando o erro de dentro de seu código. Algumas funções retornam esse erro, embora os tipos de valor e intervalos sejam permitidos, por `FIND("a","xyz")` exemplo retornam esse erro. 
  
Você deve considerar retornar esse erro da função de suplemento para indicar que os argumentos são do tipo incorreto, que não puderam ser convertidos no tipo correto ou estão fora do intervalo, embora você deva considerar o retorno de **#NUM!** para argumentos numéricos fora do intervalo. Você também deve considerar retornar esse erro quando os argumentos Range ou array forem a forma ou o tamanho errado. 
  
### <a name="ref"></a>#REF!

O Excel gera o **#REF!** erro dentro de uma expressão quando ela é copiada para um local onde a referência relativa resultante fica fora dos limites. Por exemplo, se a célula B2 contiver a `=A1`fórmula, a cópia para a célula B1 resultará em uma fórmula **= #REF!**. Esse erro também é gerado em fórmulas que contêm uma referência que é substituída em uma operação de recortar e colar ou é excluída em uma linha, coluna ou exclusão de planilha. Algumas funções que podem retornar referências podem retornar esse erro, por exemplo, `OFFSET(A1,-1,-1)`. Nomes de planilha cujas definições contêm referências que se tornam inválidas são avaliadas como esse erro.
  
Se a função do suplemento receber argumentos de referência, considere retornar esse erro se as referências forem inválidas ou se você tiver passado um erro de referência. A seção sobre XLOPER/XLOPER12s no [Gerenciamento de memória no Excel](memory-management-in-excel.md) descreve como criar funções que podem aceitar e retornar argumentos de referência. 
  
### <a name="name"></a>#NAME?

O Excel gera o **#NAME?** erro quando uma expressão contém um token que não é reconhecido como uma função ou um nome definido. Se sua função de suplemento tentar acessar um nome definido e ela não estiver definida, considere retornar esse erro. 
  
### <a name="num"></a>#NUM!

Muitas das funções numéricas e matemáticas internas no Excel retornam o **#NUM!** erro quando uma entrada numérica está fora do intervalo permitido, por exemplo, `LN(0)`. Considere retornar esse erro da função de suplemento para indicar que uma entrada numérica era inválida ou está fora do intervalo.
  
### <a name="na"></a>#N/A

O erro **#N/a** geralmente é retornado para significar que um resultado bem-sucedido ou significativo não está disponível. Por exemplo, a correspondência com o terceiro argumento zero retornará esse erro se uma correspondência exata não puder ser encontrada. Esse erro também pode ser gerado usando a função **na** e foi especificamente detectada com a função **Forna**. Portanto, é um erro comumente usado em planilhas para indicar um intervalo de condições específicas do aplicativo.
  
## <a name="see-also"></a>Confira também



[Conceitos de programação do Excel](excel-programming-concepts.md)
  
[Programação com a API de C no Excel](programming-with-the-c-api-in-excel.md)
  
[Avaliar nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)

