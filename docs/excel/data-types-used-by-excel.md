---
title: Tipos de dados usados pelo Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- registration data types [excel 2007],Excel data types,strings [Excel 2007],numbers [Excel 2007],data structures [Excel 2007],data types [Excel 2007]
localization_priority: Normal
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b32a9beb2f77c12e6b6f2c445672c717a2546386
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765271"
---
# <a name="data-types-used-by-excel"></a>Tipos de dados usados pelo Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Microsoft Excel troca v�rios tipos de ANSI C/C++ e tamb�m algumas estruturas de dados espec�ficas do Excel. Eles s�o mencionados aqui para fornecer um contexto para outras se��es e s�o abordados detalhadamente no t�pico [xlfRegister (Form 1)](xlfregister-form-1.md). 
  
## <a name="ansi-cc-types"></a>Tipos de ANSI C/C++

### <a name="numbers"></a>N�meros

Todas as vers�es do Excel:
  
- duplo de 8 bytes
    
- short [signed] [int] &ndash; usado para valores **booleanos** e também inteiros 
    
- curto n�o assinado [int]
    
- [signed long] int
    
### <a name="strings"></a>Cadeias de caracteres

Todas as vers�es do Excel:
  
- [signed] char \* &ndash; cadeias de caracteres terminada em nulo byte de até 255 caracteres
    
- unsigned char \* &ndash; cadeias de caracteres de byte de comprimento contado de até 255 caracteres
    
Iniciando em Excel�2007:
  
- não assinados curto \* &ndash; cadeias de caracteres Unicode de até 32.767 caracteres, que podem ser terminada em nulo ou comprimento contado
    
Todos os n�meros de planilha no Excel s�o armazenados como duplicatas para que ele n�o seja necess�rio (e, na verdade, introduz uma pequena sobrecarga de convers�o) para declarar fun��es de suplemento como a troca de tipos de inteiro com o Excel.
  
Onde quer que voc� esteja usando tipos de inteiro, o Excel verifica se as entradas est�o dentro dos limites do tipo e elas falhar�o com **#NUM!** se estiver fora desses limites. A exce��o � quando voc� estiver registrando uma fun��o para usar um argumento **Boolean**, implementado usando short int. Nesse caso, qualquer entrada diferente de zero � convertida em 1 e zero � passado direto. 
  
## <a name="excel-specific-data-structures"></a>Estruturas de dados específicas do Excel

Todas as vers�es do Excel:
  
- **FP** &ndash; uma estrutura de ponto flutuante de matriz bidimensional com suporte para até 65,356 linhas pelo número máximo de colunas com suporte na versão determinada do Excel. 
    
- **XLOPER** &ndash; uma estrutura de dados do tipo multi pode representar todos os tipos de dados de planilha (incluindo erros), inteiros, referências de intervalo, tipos de controle de fluxo de planilha de macro XLM e um tipo de dados binários de armazenamento interno. 
    
   > [!NOTE]
   > [!OBSERVA��O] Cadeias de caracteres s�o representadas como cadeias de caracteres de bytes contada por tamanho de at� 255 caracteres. 
  
Iniciando em Excel�2007:
  
- **FP12** &ndash; uma estrutura de ponto flutuante de matriz bidimensional com suporte para todas as linhas e colunas começando no Excel 2007. 
    
- **XLOPER12** &ndash; uma estrutura de dados do tipo multi pode representar todos os tipos de dados de planilha (incluindo erros), inteiros, referências de intervalo, tipos de controle de fluxo de planilha de macro XLM e um tipo de dados binários de armazenamento interno. 
    
   > [!NOTE]
   > [!OBSERVA��O] Cadeias de caracteres s�o representadas como cadeias de caracteres Unicode contada por tamanho de at� 32.767 caracteres. 
  
## <a name="registration-data-type-codes"></a>Códigos de tipo de dados de registro

As fun��es XLL s�o registradas com a fun��o da API C do **xlfRegister**, que usa como terceiro argumento uma cadeia de caracteres de letras que codifica os tipos de retorno e argumento. Essa cadeia de caracteres tamb�m cont�m as informa��es que indicam ao Excel se a fun��o � vol�til, se � thread-safe (iniciando em Excel�2007), se � equivalente � folha de macro e se ela retorna o resultado modificando um argumento no local.
  
A tabela a seguir � reproduzida e abordada mais detalhadamente no t�pico [xlfRegister (Form 1)](xlfregister-form-1.md). Ela � reproduzida aqui com a finalidade de fornecer um contexto para o restante desta se��o. Por exemplo, uma fun��o que usa uma cadeia de caracteres Unicode contada por tamanho (iniciando em Excel�2007) poderia ser descrita como usando um argumento do tipo C%. 
  
|Tipo de dados|Passar por valor|Passar por ref (ponteiro)|Comentários|
|:-----|:-----|:-----|:-----|
|Boolean  <br/> |A  <br/> |L  <br/> |curto (0= false ou 1= verdadeiro)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |Cadeia de byte ASCII terminada em nulo  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Comprimento-contados a cadeia de caracteres de byte ASCII  <br/> |
|não assinados curto \* (começando no Excel 2007)  <br/> ||C%, F%  <br/> |Cadeia de caracteres longa Unicode terminada em nulo  <br/> |
|não assinados curto \* (começando no Excel 2007)  <br/> ||D%, G%  <br/> |Cadeia de caracteres longa Unicode comprimento contado  <br/> |
|curto n�o assinado [int]  <br/> |H  <br/> ||WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32 bits  <br/> |
|Array  <br/> ||O  <br/> | Passados como tr�s argumentos por refer�ncia:  <br/>1. curto int \*linhas  <br/>2. curto int \*colunas  <br/>3. double \*matriz  <br/> |
|Array  <br/> (iniciando em Excel�2007)  <br/> ||O%  <br/> | Passados como tr�s argumentos por refer�ncia:  <br/>1. int \*linhas  <br/>2. int \*colunas  <br/>3. double \*matriz  <br/> |
|FP  <br/> ||K  <br/> |Estrutura de matriz de ponto flutuante  <br/> |
|FP12  <br/> (iniciando em Excel�2007)  <br/> ||K%  <br/> |Estrutura de matriz de ponto flutuante de grade grande  <br/> |
|XLOPER  <br/> ||P  <br/> |Matrizes e valores de planilha de tipo variável  <br/> |
|||L  <br/> |Valores, matrizes e referências de intervalo  <br/> |
|XLOPER12  <br/> (iniciando em Excel�2007)  <br/> ||Q  <br/> |Matrizes e valores de planilha de tipo variável  <br/> |
|||U  <br/> |Valores, matrizes e referências de intervalo  <br/> |
   
Os tipos **C%**, **F%**, **D%**, **G%**, **K%**, **O%**, **Q** e **U** eram todos novos no Microsoft Office Excel 2007 e n�o t�m suporte em vers�es anteriores. Os tipos de cadeia de caracteres **F**, **F%**, **G** e **G%** s�o usados para os argumentos que s�o modificados no local. Quando os argumentos **XLOPER** ou **XLOPER12** s�o registrados como tipos **P** ou **Q**, respectivamente, o Excel converte as refer�ncias de c�lula �nica para valores simples e refer�ncias de c�lula m�ltipla ao prepar�-las. 
  
Os tipos **P** e **Q** sempre chegam � fun��o como um dos seguintes tipos: **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing** ou **xltypeNil**, mas n�o **xltypeRef** ou **xltypeSRef**, pois s�o desreferenciados. 
  
O tipo **O**, que, na verdade, s�o tr�s argumentos na pilha, foi introduzido para compatibilidade com DLLs Fortran em que os argumentos s�o passados por refer�ncia. Ele n�o pode ser usado para retornar um valor, exceto se for usado por meio da declara��o do argumento como um valor retornado a ser modificado no local e com a coloca��o dos resultados nos valores referenciados. O tipo **O%** estende os tipos **O** no Excel�2007 para que ele possa acessar matrizes que abrangem �reas maiores do que a grade do Office Excel 2003. 
  
## <a name="see-also"></a>Ver tamb�m

- [xlfRegister (Form 1)](xlfregister-form-1.md)
- [Excel Programming Concepts](excel-programming-concepts.md)
- [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md)

