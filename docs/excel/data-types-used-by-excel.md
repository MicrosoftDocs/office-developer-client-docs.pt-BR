---
title: Tipos de dados usados pelo Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- tipos de dados de registro [Excel 2007],tipos de dados do Excel,cadeias de caracteres [Excel 2007],números [Excel 2007],estruturas de dados [Excel 2007],tipos de dados [Excel 2007]
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c546fc80b212301689744d3279a59733d9cc5524
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310903"
---
# <a name="data-types-used-by-excel"></a>Tipos de dados usados pelo Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Microsoft Excel troca vários tipos de ANSI C/C++ e também algumas estruturas de dados específicas do programa. Eles são mencionados aqui para fornecer contexto para outras seções e são abordados com detalhes no tópico [xlfRegister (Formulário 1)](xlfregister-form-1.md). 
  
## <a name="ansi-cc-types"></a>Tipos de ANSI C/C++

### <a name="numbers"></a>Números

Todas as versões do Excel:
  
- duplo de 8 bytes
    
- [signed] short [int] &ndash; usado para valores **boolianos** e inteiros 
    
- unsigned short [int]
    
- [signed long] int
    
### <a name="strings"></a>Cadeias de caracteres

Todas as versões do Excel:
  
- [signed] char \* &ndash; cadeias de caracteres de bytes terminadas por caractere nulo de até 255 caracteres
    
- unsigned char \* &ndash; cadeias de caracteres de bytes contadas por tamanho de até 255 caracteres
    
Iniciando no Excel 2007:
  
- unsigned short \* &ndash; cadeias de caracteres Unicode de até 32.767 caracteres, que podem ser terminadas por caractere nulo ou contadas por tamanho
    
Todos os números de planilha no Excel são armazenados como duplicatas para que ele não seja necessário (e, na verdade, introduz uma pequena sobrecarga de conversão) para declarar funções de suplemento como a troca de tipos de inteiro com o Excel.
  
Quando você usa tipos inteiros, o Excel verifica se as entradas estão dentro dos limites. Se não estiverem, o programa exibirá o erro **#NÚM!**. Há uma exceção quando você registra uma função para implementar um argumento **Boolean**, usando um inteiro curto. Nesse caso, qualquer entrada diferente de zero é convertida para 1, e zero é passado direto. 
  
## <a name="excel-specific-data-structures"></a>Estruturas de dados específicas do Excel

Todas as versões do Excel:
  
- **FP**&ndash; uma estrutura de matriz bidimensional de ponto flutuante com suporte para até 65.356 linhas pelo número máximo de colunas com suporte em uma versão específica do Excel. 
    
- **XLOPER**&ndash; uma estrutura de dados de vários tipos, que pode representar todos os tipos de dados de planilha (inclusive erros), inteiros, referências de intervalo, tipos de controle de fluxo de planilha de macro XLM e um tipo de dados de armazenamento binário interno. 
    
   > [!NOTE]
   > Cadeias de caracteres são representadas como cadeias de caracteres de bytes contada por tamanho de até 255 caracteres. 
  
Iniciando no Excel 2007:
  
- **FP12**&ndash; uma estrutura de matriz bidimensional de ponto flutuante com suporte para todas as linhas e colunas, iniciando no Excel 2007. 
    
- **XLOPER12**&ndash; uma estrutura de dados de vários tipos, que pode representar todos os tipos de dados de planilha (inclusive erros), inteiros, referências de intervalo, tipos de controle de fluxo de planilha de macro XLM e um tipo de dados de armazenamento binário interno. 
    
   > [!NOTE]
   > Cadeias de caracteres são representadas como cadeias de caracteres Unicode contadas por tamanho de até 32.767 caracteres. 
  
## <a name="registration-data-type-codes"></a>Códigos de tipo de dados de registro

As funções XLL são registradas com a função da API de C **xlfRegister**, que toma como terceiro argumento uma cadeia de letras que codifica os tipos de retorno e argumento. Essa sequência também contém as informações que informam ao Excel se a função é volátil, é thread-safe (iniciando no Excel 2007), é equivalente a planilhas de macro e se retorna seu resultado modificando um argumento no local.
  
Reproduzimos e abordamos a tabela a seguir com mais detalhes no tópico [xlfRegister (Formulário 1)](xlfregister-form-1.md). Ela é reproduzida aqui no intuito de fornecer contexto para o restante desta seção. Por exemplo, uma função que assume uma cadeia de caracteres Unicode contada por tamanho (iniciando no Excel 2007) poderia ser descrita como obtenção de um tipo de argumento C%. 
  
|Tipo de dados|Passar por valor|Passar por ref (ponteiro)|Comentários|
|:-----|:-----|:-----|:-----|
|Boolean  <br/> |A  <br/> |L  <br/> |curto (0= false ou 1= verdadeiro)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |Cadeia de caracteres de bytes ASCII terminada por caractere nulo  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Cadeia de caracteres de bytes ASCII contada por tamanho  <br/> |
|unsigned short \* (iniciando em Excel 2007)  <br/> ||C%, F%  <br/> |Cadeia de caracteres largos Unicode terminada por caractere nulo  <br/> |
|unsigned short \* (iniciando em Excel 2007)  <br/> ||D%, G%  <br/> |Cadeia de caracteres largos Unicode contado por tamanho  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32 bits  <br/> |
|Array  <br/> ||O  <br/> | Passados como três argumentos por referência:  <br/>1. short int \*rows  <br/>2. short int \*columns  <br/>3. double \*array  <br/> |
|Matriz  <br/> (iniciando em Excel 2007)  <br/> ||O%  <br/> | Passados como três argumentos por referência:  <br/>1. int \*rows  <br/>2. int \*columns  <br/>3. double \*array  <br/> |
|FP  <br/> ||K  <br/> |Estrutura de matriz do ponto flutuante  <br/> |
|FP12  <br/> (iniciando em Excel 2007)  <br/> ||K%  <br/> |Estrutura de matriz do ponto flutuante de grade grande  <br/> |
|XLOPER  <br/> ||P  <br/> |Valores e matrizes de planilha de tipo variável  <br/> |
|||R  <br/> |Referências de valores, matrizes e intervalos  <br/> |
|XLOPER12  <br/> (iniciando em Excel 2007)  <br/> ||I  <br/> |Valores e matrizes de planilha de tipo variável  <br/> |
|||U  <br/> |Referências de valores, matrizes e intervalos  <br/> |
   
Os tipos **C%**, **F%**, **D%**, **G%**, **K%**, **O%**, **Q** e **U** eram todos novos no Microsoft Office Excel 2007 e não têm suporte nas versões anteriores. Os tipos de cadeias de caracteres **F**, **F%**, **G** e **G%** são usados para argumentos passíveis de modificação no local. Quando os argumentos **XLOPER** ou **XLOPER12** são registrados como tipos **P** ou **Q**, respectivamente, o Excel converte as referências de célula única em valores simples e as referências de várias células em matrizes, depois de prepará-las. 
  
Os tipos **P** e **Q** chegam sempre na função como um dos seguintes tipos: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing** ou **xltypeNil**, exceto **xltypeRef** ou **xltypeSRef**, visto que estes são sempre desreferenciados. 
  
O tipo **O**, que representa realmente três argumentos na pilha, foi adicionado para compatibilidade com DLLs de Fortran, onde os argumentos são passados por referência. Ele não pode ser usado para retornar um valor, exceto se for usado por meio da declaração do argumento como um valor de retorno a ser modificado no local e com a colocação dos resultados nos valores referenciados. O tipo **O%** estende o tipo **O** no Excel 2007. Dessa forma, ele pode acessar matrizes que abrangem áreas maiores do que a grade do Office Excel 2003. 
  
## <a name="see-also"></a>Confira também

- [xlfRegister (Formulário 1)](xlfregister-form-1.md)
- [Conceitos de programação do Excel](excel-programming-concepts.md)
- [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)

