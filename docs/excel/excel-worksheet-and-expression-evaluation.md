---
title: Avaliação de expressões e planilhas do Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- avaliação de expressão [excel 2007],erros em planilhas [Excel 2007],cadeias de caracteres Unicode longas [Excel 2007],avaliando expressões [Excel 2007], avaliando planilhas [Excel 2007],avaliação de planilha [Excel 2007],erros de planilha [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cf1e0539136435f7d7df6ef348fc92ec4380e132
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427763"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Avaliação de expressões e planilhas do Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O conteúdo da célula da planilha do Microsoft Excel é avaliado em um dos quatro tipos de dados básicos:
  
- **Números**
    
- **Booliana VERDADEIRO** ou **FALSO**
    
- **Cadeias de caracteres**
    
- **Erros**
    
Matrizes de tipo misto desses tipos também podem ser inseridas em fórmulas como argumentos para funções ou como valores que abrangem mais de uma célula em uma fórmula de matriz.
  
Quando um usuário (ou uma macro de comando) inspeções algo em uma célula, o Excel tenta interpretar a entrada e exibe uma mensagem de erro se não puder. Se a entrada começar com um prefixo de cadeia de caracteres (aspas simples), o Excel coloca todos os caracteres de entrada na célula conforme fornecido, sem modificação. (O prefixo da cadeia de caracteres não é exibido.) Se a entrada começa com **=** , ou , Excel tenta interpretar a entrada como uma **+** **-** fórmula. Se a sintaxe estiver incorreta ou a avaliação for interrompida, um erro será exibido e a célula será colocada no modo de edição. Caso contrário, o Excel tentará identificar, converter e avaliar operadores e nomes de funções e seus argumentos. 
  
Os operadores são avaliados da esquerda para a direita antes da aplicação do operador. As funções são avaliadas começando com os operadores de precedência mais alta e mais internamente (mais aninhadas). Se os argumentos ou os operadores de função não puderem ser convertidos para os tipos esperados, a avaliação falhará e resulta em um **#VALUE!** . Quando um token (que não é um valor literal) não é reconhecido como uma função ou nome ou rótulo definido, a avaliação falha e resulta em um erro **#NAME?.** 
  
Se a entrada não começar com nada disso, o Excel verificará padrões conhecidos de entrada, como datas, horas, valores de moeda, porcentagens ou números, e interpretará de acordo. Isso é feito de uma maneira específica da localidade. Se nenhuma dessas interpretações fizer sentido, o Excel volta a considerar a entrada como uma cadeia de caracteres e a coloca na célula inalterada.
  
O Excel dá suporte a outros tipos de dados, sendo que o mais visível é uma referência de intervalo. O Excel converte referências aos valores das células referenciadas ao avaliar argumentos para operadores e funções que não fazem referência a argumentos ou quando a expressão em uma fórmula de célula reduz a uma referência.
  
O Excel expõe a capacidade de reduzir qualquer cadeia de caracteres válida para um dos quatro tipos de dados básicos de planilha com a função XLM **EVALUATE** e sua API C equivalente **xlfEvaluate**. Essa função fornece, entre outras coisas, uma maneira simples de avaliar intervalos nomeados no código DLL. Essa função difere do comportamento descrito anteriormente apenas porque, em vez de exibir mensagens de erro ou habilitar a edição de células, ela retorna um **#VALUE!** se a avaliação de expressão falhar. 
  
## <a name="numbers"></a>Números

Todos os números de planilha no Excel são representados internamente como ponto flutuante de precisão dupla de 8 byte, incluindo todos os inteiros. No entanto, a implementação desses números no Excel não é totalmente compatível com IEEE, conforme mostrado na tabela a seguir.
  
|**Tipo**|**Máximo**|**Minimum**|
|:-----|:-----|:-----|
|IEEE duplo de 8 byte  <br/> |1.7976931348623157E+308  <br/> |2.2250738585072014E-308  <br/> |
|Planilha (retornada por função ou valor de colar)  <br/> |1.7976931348623157E+308  <br/> |2.22507385850721E-308  <br/> |
|Planilha (entrada manual)  <br/> |9,99999999999999E+307  <br/> |2.22507385850721E-308  <br/> |
   
Os números subnormais IEEE (ou seja, números no intervalo 2,2250738585072009E-308 a 4,9406564584124654E-324) não são suportados em planilhas do Excel, mas são suportados pelo VBA Doubles.
  
Se uma função DLL retornar IEEE +/- infinito ou um duplo inválido, o Excel o converterá em **#NUM!**. Todos os números e números subnormais menores do que o normal positivo mínimo no Excel são convertidos em zero positivo. Zero negativo IEEE é suportado, ou seja, ele pode ser retornado por uma função DLL e é exibido como **-0**. (O **\<** operador não verifica se há zero negativo e, **portanto, =A1 \< 0** é avaliada como **VERDADEIRO** se A1 contiver zero negativo). 
  
Observe que determinados formatos de número têm limites mais estreitos do que esses, por exemplo, datas e horas. A divisão de números inteiros é, na verdade, a divisão de ponto flutuante e pode, em casos extremos, gerar um resultado não inteiro em que o resultado preciso deve ser um inteiro.
  
## <a name="long-unicode-strings"></a>Cadeias de caracteres Unicode longas

Todas as cadeias de caracteres que o usuário vê no Excel têm para muitas versões agora foram armazenadas internamente como cadeias de caracteres Unicode. As cadeias de caracteres da planilha Unicode podem ter até 32.767 (2<sup>15</sup> - 1) caracteres de comprimento e podem conter qualquer caractere Unicode válido. 
  
Quando a API de C foi introduzida pela primeira vez, as cadeias de caracteres de planilha eram cadeias de caracteres de byte limitadas a 255 caracteres, e a API de C refletia essas limitações. Com o Excel 2007, a API de C é atualizada para lidar com cadeias de caracteres Unicode longas do Excel. Isso significa que as funções DLL registradas da maneira certa podem aceitar argumentos Unicode e retornar cadeias de caracteres Unicode.
  
> [!NOTE]
> As cadeias de caracteres de byte ainda têm suporte total na API de C para compatibilidade com compatibilidade com trás; no entanto, eles ainda têm o mesmo limite de 255 caracteres. 
  
## <a name="returning-errors"></a>Retornando erros

O Excel avalia células como erros em que não pode converter argumentos de operador ou função para o tipo correto ou se não reconhece uma função ou nome definido. Esses dois cenários foram descritos anteriormente. Quando as funções e operadores de planilha internas falham, eles também resultam em erros que informam o usuário sobre o tipo de falha. Você deve fazer com que suas próprias funções de complemento retornem erros consistentes com o comportamento no Excel.
  
### <a name="null"></a>#NULL!

O **#NULL!** é retornado por algumas funções de informações XLM. Por exemplo, chamar **GET.DOCUMENT(78)** ou a função equivalente da API C **xlfGetDocument** com o argumento 78, quando não houver impressoras instaladas, esse erro será retornado. Ele também pode ser retornado por algumas funções quando, por exemplo, eles avaliam uma cadeia de caracteres vazia. 
  
Talvez você queira retornar esse erro da função do seu complemento quando nenhum dos outros erros parecer apropriado.
  
### <a name="div0"></a>#DIV/0!

O operador de divisão do Excel retorna **o #DIV/0!** quando o denominador é avaliada como zero ou um número é muito pequeno para ser representado como não zero pelo Excel. Algumas funções que, por definição, envolvem uma divisão também podem retornar esse erro. Por exemplo, **MÉDIA** retornará esse erro se nenhuma das entradas puder ser convertida em números. 
  
Você só deve considerar retornar esse erro de sua função de complemento para indicar que uma divisão por zero foi detectada.
  
### <a name="value"></a>#VALUE!

O Excel retorna o **#VALUE!** se um argumento de função ou operador não puder ser convertido para o tipo necessário. No caso de argumentos de função que não podem ser convertidos, por  `=LN("X")` exemplo, o Excel não chama o código de função. Esse é um ponto importante a ser lembrado ao escrever e depurar suas próprias funções de complemento. 
  
Algumas funções retornarão esse erro se um argumento não puder ser convertido dentro do código de função. Por exemplo,  `DATEVALUE("30-Feb-2007")` falha com esse erro apesar do argumento ser do tipo certo. Nesse caso, é a função que está retornando o erro de dentro de seu código. Algumas funções retornam esse erro mesmo que os tipos de valor e intervalos sejam perecíveis, por  `FIND("a","xyz")` exemplo, retorna esse erro. 
  
Você deve considerar retornar esse erro da sua função de add-in para indicar que os argumentos são do tipo errado, não pode ser convertido para o tipo certo ou estão fora do intervalo, embora você deva considerar retornar **#NUM!** para argumentos numéricos fora do intervalo. Você também deve considerar retornar esse erro quando os argumentos de intervalo ou matriz são a forma ou o tamanho errados. 
  
### <a name="ref"></a>#REF!

O Excel gera o **#REF!** em uma expressão quando ela é copiada para um local onde a referência relativa resultante sai dos limites. Por exemplo, se a célula B2 contiver a fórmula, copiá-lo para a célula B1 resulta em uma  `=A1` fórmula **=#REF!**. Esse erro também é gerado em fórmulas que contêm uma referência que é substituída em uma operação recortar e colar ou é excluída em uma linha, coluna ou exclusão de planilha. Algumas funções que podem retornar referências podem retornar esse erro, por exemplo,  `OFFSET(A1,-1,-1)` . Os nomes das planilhas cujas definições contêm referências que se tornam inválidas são avaliados por esse erro.
  
Se a função do seu complemento tiver argumentos de referência, você deve considerar retornar esse erro se as referências são inválidas ou se você tiver passado um erro de referência. A seção sobre XLOPER/XLOPER12s no Gerenciamento de Memória no [Excel](memory-management-in-excel.md) descreve como criar funções que podem aceitar e retornar argumentos de referência. 
  
### <a name="name"></a>#NAME?

O Excel gera o **#NAME?** quando uma expressão contém um token que não é reconhecido como uma função ou nome definido. Se a função de seu complemento tentar acessar um nome definido e não estiver definido, considere retornar esse erro. 
  
### <a name="num"></a>#NUM!

Muitas das funções numéricas e matemáticas no Excel retornam o **#NUM!** quando uma entrada numérica está fora do intervalo permitido, por exemplo,  `LN(0)` . Você deve considerar retornar esse erro da função do seu complemento para indicar que uma entrada numérica era inválida ou fora do intervalo.
  
### <a name="na"></a>#N/A

O **#N/A** geralmente é retornado para significar que um resultado bem-sucedido ou significativo não está disponível. Por exemplo, MATCH com o terceiro argumento zero retornará esse erro se uma combinação exata não puder ser encontrada. Esse erro também pode ser gerado usando a função **NA** e especificamente detectado com a função **ISNA**. Portanto, é um erro comumente usado em planilhas para indicar um intervalo de condições específicas do aplicativo.
  
## <a name="see-also"></a>Confira também



[Conceitos de programação do Excel](excel-programming-concepts.md)
  
[Programação com a API de C no Excel](programming-with-the-c-api-in-excel.md)
  
[Avaliar nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)

