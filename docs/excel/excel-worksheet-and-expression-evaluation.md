---
title: Planilha do Excel e avaliação de expressões
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- avaliação da expressão [excel 2007], erros em planilhas [Excel 2007], tempo cadeias de caracteres Unicode [Excel 2007], avaliando expressões [Excel 2007], avaliando planilhas [Excel 2007], avaliação de planilha [Excel 2007], erros de planilha [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 543ff7fcbc88253dafd7fc6e7000bf9657d8c258
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765346"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Planilha do Excel e avaliação de expressões

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Conteúdo de células de planilha do Microsoft Excel é avaliado em uma destas quatro tipos de dados básicos:
  
- **N�meros**
    
- **Boolean TRUE** ou **FALSE**
    
- **Cadeias de Caracteres**
    
- **Erros**
    
Matrizes de tipo misto desses tipos também podem ser inseridos em fórmulas como argumentos para funções ou como abrangendo mais de uma célula em uma fórmula de matriz de valores.
  
Quando um usuário (ou uma macro de comando) insere algo em uma célula, o Excel tenta interpretar a entrada e exibe uma mensagem de erro, se ele não pode. Se a entrada começa com um prefixo de cadeia de caracteres (aspas simples) Excel coloca todos os caracteres de entrada na célula disposto, sem modificações. (O prefixo de cadeia de caracteres não é exibido). Se a entrada começa com **=**, **+**, ou **-**, Excel tenta interpretar a entrada como uma fórmula. Se a sintaxe está incorreta ou avaliação estiver parada, um erro é exibido e a célula é colocada modo de edição. Caso contrário, Excel tenta identificar, converter e avaliar os operadores e nomes de função e seus argumentos. 
  
Operandos são avaliados da esquerda para direita antes do operador é aplicado. Funções são avaliadas começando com os operadores de precedência mais alta e mais interno (mais aninhadas). Se os argumentos da função ou operandos não podem ser convertidos para os tipos de esperado, avaliação falhará e resultará em um **#VALUE!** erro. Quando um token (que não é um valor literal) não é reconhecido como uma função ou o nome definido ou rótulo, avaliação falhará e resultará em um **#NAME?** erro. 
  
Se a entrada não for iniciado com qualquer uma dessas coisas, o Excel verifica a padrões conhecidos de entrada, como datas, horas, valores de moeda, porcentagens ou números e interpreta adequadamente. Isso é feito de uma forma específica de localidade. Se nenhum desses interpretações faz sentido, Excel reverterá para considerar a entrada como uma cadeia de caracteres e o coloca na célula inalterada.
  
Excel oferece suporte a outros tipos de dados, o mais visíveis for uma referência de intervalo. Excel converte referências para os valores das células referenciadas ao avaliar argumentos para operadores e funções que não usa argumentos de referência, ou quando a expressão em uma fórmula de célula reduz a uma referência.
  
Excel expõe a capacidade de reduzir qualquer cadeia de caracteres válida para um dos tipos de dados de planilha quatro básica com a função XLM **EVALUATE** e seu equivalente do C API **xlfEvaluate**. Entre outras coisas, essa função fornece uma maneira simple para avaliar a intervalos nomeados em código DLL. Essa função difere do comportamento descrito anteriormente somente em que, em vez de exibir mensagens de erro ou ativar a edição de célula, ele retorna uma **#VALUE!** erro se a avaliação da expressão falhar. 
  
## <a name="numbers"></a>N�meros

Todos os números de planilha do Excel são representados internamente como 8 bytes double ponto flutuante de precisão, incluindo todos os inteiros. No entanto, a implementação desses números no Excel não é totalmente compatível com, IEEE conforme mostrado na tabela a seguir.
  
|**Tipo**|**Maximum**|**Mínimo**|
|:-----|:-----|:-----|
|Dupla de 8 bytes IEEE  <br/> |1.7976931348623157E + 308  <br/> |2.2250738585072014E-308  <br/> |
|Planilha (retornada pela função ou colar valor)  <br/> |1.7976931348623157E + 308  <br/> |2.22507385850721E-308  <br/> |
|Planilha (entrada manual)  <br/> |9.99999999999999E + 307  <br/> |2.22507385850721E-308  <br/> |
   
Números de subnormal IEEE (ou seja, números no intervalo 2.2250738585072009E-308 para 4.9406564584124654E-324) não são suportados em planilhas do Excel, mas são suportados pelo VBA duplicatas.
  
Se uma função DLL retorna IEEE + /-infinito ou um double inválido, o Excel converte em **#NUM!**. Subnormal todos os números e números menores do que o mínimo normais positivo no Excel são convertidos em zero positivo. IEEE zero negativo é suportada, ou seja, ele pode ser retornado por uma função de DLL e é exibido como **-0**. (O **\<** operador não verifica a zero negativo e isso **= A1\<0** é avaliada como **TRUE** se A1 contiver zero negativo). 
  
Observe que certos formatos de número tem limites mais estreitos que esses, por exemplo, datas e horas. Divisão de inteiro é, na verdade, divisão de ponto flutuante e poderia, em casos extremos, gerar um resultado não inteiro onde o resultado preciso deve ser um inteiro.
  
## <a name="long-unicode-strings"></a>Cadeias de caracteres Unicode longo

Todas as cadeias de caracteres que o usuário vê no Excel para várias versões agora foram armazenadas internamente como sequências de caracteres Unicode. Cadeias de caracteres Unicode planilha podem ser até 32.767 (2<sup>15</sup> - 1) caracteres e pode contenham qualquer caractere Unicode válido. 
  
Quando a API C foi primeira introduzido, cadeias de caracteres de planilha foram cadeias de caracteres de byte limitadas a 255 caracteres, e a API C reflete estas limitações. Com o Excel 2007, a API C é atualizada para lidar com cadeias de caracteres do Excel de longas Unicode. Isso significa que funções DLL registradas na forma certa podem aceitar argumentos Unicode e retornar as cadeias de caracteres Unicode.
  
> [!NOTE]
> Cadeias de caracteres de byte ainda totalmente são suportadas do C API para compatibilidade com versões anteriores; No entanto, eles ainda têm o mesmo limite de 255 caracteres. 
  
## <a name="returning-errors"></a>Retornando erros

Excel avalia as células a erros onde argumentos da função ou operador não pode converter para o tipo correto, ou se ele não reconhecer uma função ou o nome definido. Esses dois cenários foram descritos anteriormente. Quando as funções de planilha internas e operadores falham, eles também resultam em erros que informam ao usuário do tipo de falha. Você deve ter suas próprias funções suplemento retorna erros que são consistentes com o comportamento no Excel.
  
### <a name="null"></a>#NULL!

O **#NULL!** erro será retornado por algumas funções de informações XLM. Por exemplo, chamando **GET. Document(78)**, ou equivalente API C funcionar **xlfGetDocument** com o argumento 78, quando não há nenhum resultado impressoras instaladas nesse erro sendo retornado. Ele também pode ser retornado com algumas funções quando, por exemplo, eles avaliar uma sequência vazia. 
  
Talvez você queira retornar esse erro de sua função de suplemento quando nenhum dos outros erros parece adequado.
  
### <a name="div0"></a>#DIV/0!

O operador de divisão de Excel retorna o **#DIV/0!** Quando denominador é avaliada como zero ou um número de erro é muito pequeno para ser representado como diferente de zero pelo Excel. Algumas funções que, por definição, envolvem uma divisão também podem retornar esse erro. Por exemplo, **média** retorna este erro se nenhuma das entradas podem ser convertidas em números. 
  
Você só deve considerar retornando esse erro de sua função suplemento para indicar que uma divisão por zero foi detectada.
  
### <a name="value"></a>#VALUE!

Excel retorna o **#VALUE!** erro, se um argumento de função ou operador não puder ser convertido para o tipo necessário. No caso de argumentos da função que não podem ser convertidos, por exemplo `=LN("X")`, Excel não chamar o código de função. Este é um ponto importante a lembrar ao escrever e depurar suas próprias funções do suplemento. 
  
Algumas funções retornam esse erro se um argumento não puder ser convertido no código da função. Por exemplo, `DATEVALUE("30-Feb-2007")` falhar com esse erro, apesar do argumento sendo do tipo à direita. Nesse caso, é a função que está retornando o erro de dentro de seu código. Algumas funções retornam esse erro, mesmo que os tipos de valores e intervalos são permitidos, por exemplo `FIND("a","xyz")` retorna este erro. 
  
Você deve considerar a retornar esse erro de sua função suplemento para indicar que os argumentos são do tipo incorreto, não pôde ser convertido para o tipo de direito ou estiver fora do intervalo, embora você deve considerar retornando **#NUM!** para argumentos numéricos fora do intervalo. Você também deve considerar retornando esse erro quando a matriz ou intervalo de argumentos são a forma errada ou o tamanho. 
  
### <a name="ref"></a>#REF!

Excel gerará o **#REF!** Erro dentro de uma expressão quando ele é copiado para um local onde a referência relativa resultante vai fora dos limites. Por exemplo, se a célula B2 contém a fórmula `=A1`, copiando isso à célula B1 resulta em uma fórmula **= #REF!**. Esse erro também é gerado em fórmulas que contêm uma referência que será substituída em uma operação de recortar e colar ou é excluída em uma linha, coluna ou exclusão da planilha. Algumas funções que podem retornar referências podem retornar esse erro, por exemplo, `OFFSET(A1,-1,-1)`. Nomes de planilha cujas definições contêm referências que se tornam inválidas são avaliados para esse erro.
  
Se sua função suplemento utiliza argumentos de referência, você deve considerar a retornar esse erro, se as referências forem inválidas, ou se você estiver passado um erro de referência. A seção sobre XLOPER/XLOPER12s no [Gerenciamento de memória no Excel](memory-management-in-excel.md) descreve como criar funções que podem aceitar e retornar referência argumentos. 
  
### <a name="name"></a>#NAME?

Excel gerará o **#NAME?** erro quando uma expressão contém um token que não seja reconhecido como uma função ou o nome definido. Se sua função suplemento tenta acessar um nome definido e ele não for definido, você deve considerar a retornar esse erro. 
  
### <a name="num"></a>#NUM!

Muitas das funções numéricas e matemáticas internas em retorno do Excel a **#NUM!** erro quando uma entrada numérica estiver fora do intervalo permitido, por exemplo, `LN(0)`. Você deve considerar retornando esse erro de sua função suplemento para indicar que uma entrada numérica era inválida ou fora do intervalo.
  
### <a name="na"></a>#N/A

O erro **# N/d** frequentemente é retornado para indicar que um resultado bem-sucedido ou significativo não está disponível. Por exemplo, a correspondência com o terceiro argumento zero retorna este erro se não for encontrada uma correspondência exata. Esse erro também pode ser gerado usando a função **NA** e especificamente detectado com a função **disp**. Portanto, é um erro de comumente usado em planilhas para indicar uma gama de condições específicas do aplicativo.
  
## <a name="see-also"></a>Confira também



[Excel Programming Concepts](excel-programming-concepts.md)
  
[Programar com a API de C no Excel](programming-with-the-c-api-in-excel.md)
  
[Avaliar nomes e outras expressões de fórmula de planilha](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)

