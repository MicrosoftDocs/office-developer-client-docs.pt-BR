---
title: LIKE (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Determina se uma cadeia de caracteres específica corresponde a um padrão especificado. Um padrão pode incluir caracteres regulares e caracteres curinga. Durante a correspondência de padrões, os caracteres regulares devem corresponder exatamente aos caracteres especificados na cadeia de caracteres. No entanto, caracteres curinga podem ser encontrados com fragmentos arbitrários da cadeia de caracteres. Usar caracteres curinga torna o operador LIKE mais flexível do que usar os operadores de comparação de cadeia de caracteres = e !=.
ms.openlocfilehash: 02d1e4f8fc61335e828a1f77579c14b1c7577485
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406112"
---
# <a name="like-access-custom-web-app"></a>LIKE (aplicativo Web personalizado do Access)

Determina se uma cadeia de caracteres específica corresponde a um padrão especificado. Um padrão pode incluir caracteres regulares e caracteres curinga. Durante a correspondência de padrões, os caracteres regulares devem corresponder exatamente aos caracteres especificados na cadeia de caracteres. No entanto, caracteres curinga podem ser encontrados com fragmentos arbitrários da cadeia de caracteres. Usar caracteres curinga torna o **operador LIKE** mais flexível do que usar os operadores de comparação de cadeia de caracteres = e !=. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 *Expression*  [ NOT ] **LIKE** *Pattern*  [ ESCAPE  *EscapeChar*  ] 
  
O **operador LIKE** contém os seguintes argumentos 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| *Expressão*.  <br/> |Sim  <br/> |Uma expressão válida.  <br/> |
| *Padrão de*  <br/> |Sim  <br/> |A cadeia de caracteres específica a ser pesquisada em  *Expression*  . Pode incluir caracteres curinga. Consulte os Comentários para ver uma lista de caracteres curinga válidos.  <br/> |
| *EscapeChar*  <br/> |Não  <br/> |Um caractere que é colocado na frente de um caractere curinga para indicar que o caractere curinga deve ser interpretado como um caractere regular e não como um caractere curinga.  *EscapeChar*  é uma expressão de caractere que não tem padrão e deve ser avaliada como apenas um caractere.  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir contém os caracteres curinga que são válidos para uso no *argumento Pattern.* 
  
|**Caractere curinga**|**Descrição**|**Exemplo**|
|:-----|:-----|:-----|
|%  <br/> |Qualquer cadeia de caracteres de zero ou mais caracteres.  <br/> | *WHERE title LIKE '%computer%'*  finds all book titles with the word 'computer' anywhere in the book title.  <br/> |
|_ (sublinhado)  <br/> |Qualquer caractere simples.  <br/> | *WHERE au_fname LIKE '_ean'*  localiza todos os nomes de quatro letras que terminam com ean (Time, Time e assim por diante).  <br/> |
|[]  <br/> |Qualquer caractere único dentro do intervalo especificado ([a-f]) ou conjunto ([abcdef]).  <br/> | *WHERE au_lname LIKE '[C-P]arsen'*  localiza os sobrenomes do autor terminando com arsen e começando com qualquer caractere único entre C e P, por exemplo Carsen, Boo, Karsen e assim por diante.  <br/> |
|[^]  <br/> |Qualquer caractere único que não está dentro do intervalo especificado ([^a-f]) ou definido ([^abcdef]).  <br/> | *WHERE au_lname LIKE 'de[^l]%'*  all author last names starting with de and where the following letter is not l.  <br/> |
   
Quando você executa comparações de cadeia de caracteres usando **LIKE**, todos os caracteres na cadeia de caracteres padrão são significativos. Isso inclui espaços à frente ou à trailing. Se uma comparação em uma consulta for retornar todas as linhas com uma cadeia de caracteres **LIKE** 'abc ' (abc seguida de um único espaço), uma linha na qual o valor dessa coluna é abc (abc sem um espaço) não será retornada. No entanto, espaços em branco à parte, na expressão à qual o padrão é corresponder, são ignorados. Se uma comparação em uma consulta for retornar todas as linhas com a cadeia de caracteres **LIKE** 'abc' (abc sem um espaço), todas as linhas que começam com abc e têm zero ou mais espaços em branco à esquerda serão retornadas. 
  
Se qualquer um dos argumentos não for de um tipo de dados de cadeia de caracteres, ele será convertido em um tipo de dados de cadeia de caracteres, se possível.
  

