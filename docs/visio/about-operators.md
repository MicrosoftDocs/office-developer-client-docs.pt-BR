---
title: Sobre Operadores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251824
localization_priority: Normal
ms.assetid: 43128ea2-c0d9-c45f-31e6-768a80ae59b2
description: Você pode usar operadores em fórmulas para executar operações aritméticas (adição, subtração, multiplicação etc.) ou comparações lógicas (maior que, menor que, igual a etc.). Além disso, pode controlar a ordem de avaliação em uma fórmula incluindo expressões entre parênteses. Use o operador E comercial para combinar (concatenar) cadeias de caracteres.
ms.openlocfilehash: 4f095df73f9bd1d6a876d975d262c9217c696fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406126"
---
# <a name="about-operators"></a>Sobre Operadores

Você pode usar operadores em fórmulas para executar operações aritméticas (adição, subtração, multiplicação etc.) ou comparações lógicas (maior que, menor que, igual a etc.). Além disso, pode controlar a ordem de avaliação em uma fórmula incluindo expressões entre parênteses. Use o operador E comercial para combinar (concatenar) cadeias de caracteres.
  
O Microsoft Visio tenta converter automaticamente os tipos de dados quando uma operação ou função necessita de um tipo de dado específico. Por exemplo, o operador de multiplicação necessita de argumentos numéricos e o operador de E comercial (concatenação de cadeia de caracteres), de argumentos de cadeia de caracteres. Se o argumento não puder ser convertido para o tipo de dado necessário, um valor padrão será fornecido. O valor padrão é o equivalente digitado para nada: zero para números, FALSO para valores boolianos, ""; para cadeias de caracteres etc.
  
A tabela a seguir mostra exemplos de expressões e seus resultados.
  
|**Expressão**.|**Resultado**|**Descrição**|
|:-----|:-----|:-----|
| 2 \* 5 &amp; "centavos"  <br/> | "10 centavos"  <br/> | O &amp; operador (concatenação de cadeia de caracteres) requer argumentos de cadeia de caracteres, \* portanto, o resultado numérico de 2 5 é convertido automaticamente na cadeia de caracteres "10".  <br/> |
| 5 \* "2"  <br/> | 10   <br/> | O \* operador (multiplicação) requer argumentos numéricos, portanto, a cadeia de caracteres "2" é automaticamente convertida para o número 2 equivalente.  <br/> |
| 5 \* "ovelha"  <br/> | ,0  <br/> | O \* operador (multiplicação) requer argumentos numéricos, portanto, porque a cadeia de caracteres "ovelha" não pode ser convertida para um número, zero é usado como seu equivalente numérico.  <br/> |
   
## <a name="arithmetic-operators"></a>Operadores aritméticos

Os operadores aritméticos executam operações em números. Os operadores de mais (+) e menos (-) podem ser utilizados sozinhos como operadores unários para determinar o sinal de um número. O operador de por cento (%) também é um operador unário e identifica o número como uma porcentagem.
  
|**Operador**|**Action**|**Exemplo**|**Resultado**|
|:-----|:-----|:-----|:-----|
| +  <br/> | Mais unário  <br/> | + 37  <br/> | 37  <br/> |
| -  <br/> | Menos unário  <br/> | -37  <br/> | -37  <br/> |
| %  <br/> | Porcentagem unária  <br/> | 37%  <br/> | .37  <br/> |
| ^  <br/> | Exponencial  <br/> | 5 ^ 2  <br/> | 25  <br/> |
| \*  <br/> | Multiplicação  <br/> | 5 \* 2  <br/> | 10   <br/> |
| /  <br/> | Divisão  <br/> | 5 / 2  <br/> | 2.5  <br/> |
| +  <br/> | Adição  <br/> | 5 + 2  <br/> | 7   <br/> |
| -  <br/> | Subtração  <br/> | 5 - 2  <br/> | 3D  <br/> |
   
## <a name="comparison-operators"></a>Operadores de comparação

Os operadores de comparação são utilizados para a criação de expressões lógicas. Uma expressão lógica pode ser avaliada como VERDADEIRO ou FALSO.
  
|**Operador**|**Alternativas**|**Action**|**Exemplo**|**Resultado**|
|:-----|:-----|:-----|:-----|:-----|
| \>  <br/> | _GT_  <br/> | Maior que  <br/> | 5 \> 2  <br/> | TRUE  <br/> |
| \<  <br/> | _<_  <br/> | Menor que  <br/> | 5 \< 2  <br/> | FALSE  <br/> |
| \>=  <br/> | _PÁ_  <br/> | Maior que ou igual a  <br/> | 5 \>= 2  <br/> | TRUE  <br/> |
| \<=  <br/> | _QUIVO_  <br/> | Menor que ou igual a  <br/> | 5 \<= 2  <br/> | FALSE  <br/> |
| =  <br/> | _ESTÚDIO_  <br/> | É igual a  <br/> | 5 = 2  <br/> | FALSE  <br/> |
| \<\>  <br/> | _PRÓXIMO_  <br/> | É diferente de  <br/> | 5 \< \> 2  <br/> | TRUE  <br/> |
   
Os operadores de comparação simbólico\>( \<, e assim por diante) são a melhor opção para a maioria das comparações. Os operadores alternativos (_gt_, _lt_e assim por diante) realizam uma comparação exata com 15 dígitos inteiros de precisão que o Visio usa para armazenar valores internamente.
  
Ao comparar valores arredondados ou calculados utilizando os operadores alternativos, FALSO pode ser retornado, quando para todos os objetivos práticos a expressão deveria ser avaliada como VERDADEIRO.
  
Quando operadores de comparação são utilizados para comparar cadeias de caracteres, estas são primeiramente convertidas para valores numéricos. As cadeias que não puderem ser convertidas, retornarão um valor de 0; consequentemente, as comparações variam e podem não apresentar os resultados esperados. Para realizar uma comparação de cadeias padrão, use as funções STRSAME ou STRSAMEEX.
  
## <a name="order-of-evaluation"></a>Ordem de avaliação

Quando uma fórmula contém mais de uma expressão, as expressões são avaliadas em ordem de acordo com a operação que está sendo executada. A tabela a seguir mostra a ordem de avaliação dos operadores no Visio.
  
|**Order**|**Action**|**Operador**|
|:-----|:-----|:-----|
|Primeiro  <br/> |Positivo  <br/> |+ (unário)  <br/> |
||Negativo  <br/> |- (unário)  <br/> |
||Por cento  <br/> |% (unário)  <br/> |
|Segundo  <br/> |Exponencial  <br/> |^  <br/> |
|Terceira  <br/> |Multiplicação  <br/> |\*  <br/> |
||Divisão  <br/> |/  <br/> |
|Etapa  <br/> |Adição  <br/> |+  <br/> |
||Subtração  <br/> |-  <br/> |
|Quinto  <br/> |Concatenação de cadeia de caracteres  <br/> |&amp;  <br/> |
|Sexto  <br/> |Maior que  <br/> |\>ou GT  <br/> |
||Maior que ou igual a  <br/> |\>= ou GE  <br/> |
||Menor que  <br/> |\<ou LT  <br/> |
||Menor que ou igual a  <br/> |\<= ou LE  <br/> |
|Sétimo  <br/> |Igual a  <br/> |= ou EQ  <br/> |
||Diferente  <br/> |\<\>ou NE  <br/> |
   
Você pode alterar a ordem de avaliação incluindo expressões entre parênteses. O Visio avalia as expressões entre parênteses primeiro, da esquerda para a direita. Por exemplo:
  
4 + 5 \* 6 = 4 + 30 = 34
  
(4 + 5) \* 6 = 9 \* 6 = 54
  
Se as expressões entre parênteses estiverem aninhadas, a expressão no conjunto de parênteses mais interno será avaliada primeiro.
  
## <a name="ampersand-operator"></a>Operador E comercial

O operador E comercial retorna uma nova cadeia de caracteres. É possível criar palavras compostas e frases usando o operador E comercial. Use a sintaxe a seguir:
  
"seqüência1" &amp; "seqüência2"
  
 **Exemplo**
  
"cachorro" &amp; "House" retorna "Doghouse"
  

