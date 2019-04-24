---
title: LIKE (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Determina se uma cadeia de caracteres específica corresponde a um padrão especificado. Um padrão pode incluir caracteres regulares e caracteres curinga. Durante a correspondência de padrões, os caracteres regulares devem corresponder exatamente aos caracteres especificados na sequência de caracteres. No enTanto, os caracteres curinga podem ser correspondidos com fragmentos arbitrários da cadeia de caracteres. O uso de caracteres curinga torna o operador LIKE mais flexível do que o uso dos operadores de comparação de cadeia de caracteres = e! =.
ms.openlocfilehash: 02d1e4f8fc61335e828a1f77579c14b1c7577485
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311078"
---
# <a name="like-access-custom-web-app"></a>LIKE (aplicativo Web personalizado do Access)

Determina se uma cadeia de caracteres específica corresponde a um padrão especificado. Um padrão pode incluir caracteres regulares e caracteres curinga. Durante a correspondência de padrões, os caracteres regulares devem corresponder exatamente aos caracteres especificados na sequência de caracteres. No enTanto, os caracteres curinga podem ser correspondidos com fragmentos arbitrários da cadeia de caracteres. O uso de caracteres curinga torna o operador **like** mais flexível do que o uso dos operadores de comparação de cadeia de caracteres = e! =. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 *Expressão*  SIDO **Como** *Padrão*  [ESCAPE *EscapeChar* ] 
  
O operador **like** contém os seguintes argumentos 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| *Expressão*  <br/> |Sim  <br/> |Uma expressão válida.  <br/> |
| *Padrão de*  <br/> |Sim  <br/> |A cadeia de caracteres específica a ser pesquisada na *expressão* . Pode incluir caracteres curinga. Consulte os comentários para obter uma lista de caracteres curinga válidos.  <br/> |
| *EscapeChar*  <br/> |Não  <br/> |Um caractere colocado na frente de um caractere curinga para indicar que o caractere curinga deve ser interpretado como um caractere regular e não como um caractere curinga.  *EscapeChar* é uma expressão Character que não tem default e deve ser avaliada como apenas um caractere.  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir contém os caracteres curinga válidos para uso no argumento *padrão* . 
  
|**Caractere curinga**|**Descrição**|**Exemplo**|
|:-----|:-----|:-----|
|%  <br/> |Qualquer sequência de zero ou mais caracteres.  <br/> | *Onde título como '% computador% '* localiza todos os títulos de livros com a palavra ' computador ' em qualquer lugar no título do livro.  <br/> |
|_ (sublinhado)  <br/> |Qualquer caractere simples.  <br/> | *Onde au_fname, como ' _ean '* , localizam todos os nomes de quatro letras que terminam com o EAN (diretora, Sílvio e assim por diante).  <br/> |
|[]  <br/> |Qualquer caractere único dentro do intervalo especificado ([a-f]) ou Set ([abcdef]).  <br/> | *Em que AU_LNAME like ' [C-P] grosseiran '* localiza os nomes de sobrenome finais com baixo e começando com qualquer caractere único entre C e P, por exemplo, Cars, Larsen, Karsen e assim por diante.  <br/> |
|[^]  <br/> |Qualquer caractere único que não esteja dentro do intervalo especificado ([^ a-f]) ou definido ([^ abcdef]).  <br/> | *Onde AU_LNAME como ' de [^ l]% '* todos os sobrenomes do autor começam com de e onde a seguinte letra não é l.  <br/> |
   
Quando você realiza comparações de cadeia de caracteres usando **like**, todos os caracteres na cadeia de caracteres de padrão são significativos. Isso inclui espaços à esquerda ou à direita. Se uma comparação em uma consulta for retornar todas as linhas com uma cadeia de caracteres **como** "ABC" (ABC seguido por um único espaço), uma linha na qual o valor dessa coluna é ABC (ABC sem um espaço) não será retornado. No enTanto, os espaços em branco à direita, na expressão à qual o padrão corresponde, são ignorados. Se uma comparação em uma consulta for retornar todas as linhas com a cadeia de caracteres **como** "ABC" (ABC sem um espaço), todas as linhas que iniciarem com a ABC e terão zero ou mais brancos à direita serão retornadas. 
  
Se qualquer um dos argumentos não for de um tipo de dados de cadeia de caracteres, ele será convertido em um tipo de dados de cadeia de caracteres, se possível.
  

