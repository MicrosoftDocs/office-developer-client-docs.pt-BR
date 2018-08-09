---
title: COMO (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Determina se uma cadeia de caracteres específica corresponde a um padrão especificado. Um padrão pode incluir caracteres regulares e caracteres curinga. Durante a correspondência de padrões, caracteres regulares devem corresponder exatamente os caracteres especificados na sequência de caracteres. No entanto, caracteres curinga podem ser comparadas com o arbitrários fragmentos da sequência de caracteres. Usando caracteres curinga torna o operador LIKE mais flexível do que usando o = e! = operadores de comparação de cadeia de caracteres.
ms.openlocfilehash: d3224647c621b05a08bdc863939d0cccae214463
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765110"
---
# <a name="like-access-custom-web-app"></a>COMO (aplicativo da web personalizado do Access)

Determina se uma cadeia de caracteres específica corresponde a um padrão especificado. Um padrão pode incluir caracteres regulares e caracteres curinga. Durante a correspondência de padrões, caracteres regulares devem corresponder exatamente os caracteres especificados na sequência de caracteres. No entanto, caracteres curinga podem ser comparadas com o arbitrários fragmentos da sequência de caracteres. Usando caracteres curinga torna o operador **LIKE** mais flexível do que usando o = e! = operadores de comparação de cadeia de caracteres. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 *Expressão*  [NOT] **Como** *Padrão*  [ESCAPE *EscapeChar* ] 
  
O operador **LIKE** contém os seguintes argumentos 
  
|**Nome do argumento**|**Obrigatório**|**Descrição**|
|:-----|:-----|:-----|
| *Expressão*  <br/> |Sim  <br/> |Uma expressão válida.  <br/> |
| *Pattern*  <br/> |Sim  <br/> |A cadeia de caracteres específica de caracteres a ser pesquisado na *expressão* . Pode incluir caracteres curinga. Consulte os comentários para obter uma lista dos caracteres curinga válidos.  <br/> |
| *EscapeChar*  <br/> |Não  <br/> |Um caractere que é colocado na frente de um caractere curinga para indicar que o caractere curinga deve ser interpretado como um caractere normal e não como um caractere curinga.  *EscapeChar* é uma expressão de caractere que não possui padrão e deve ser avaliada como apenas um caractere.  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir contém os caracteres curinga que são válidos para uso no argumento *padrão* . 
  
|**Caractere curinga**|**Descrição**|**Exemplo**|
|:-----|:-----|:-----|
|%  <br/> |Qualquer cadeia de caracteres zero ou mais.  <br/> | *Onde título como '% % do computador'* localiza todos os títulos de livros com a palavra 'computador' em qualquer lugar do título do livro.  <br/> |
|_ (sublinhado)  <br/> |Qualquer caractere simples.  <br/> | *WHERE au_fname como '_ean'* localiza todos os nomes de primeira letra quatro que terminam com ean (Dean, Sílvio e assim por diante).  <br/> |
|[]  <br/> |Qualquer único caractere dentro do intervalo especificado ([a-f]) ou definir ([abcdef]).  <br/> | Localiza *au_lname WHERE como '[C-P] arsen'* originar sobrenomes terminem com arsen e começando com qualquer caractere único entre C e P, por exemplo, Carsen, Larsen, Karsen e assim por diante.  <br/> |
|[^]  <br/> |Qualquer caractere não dentro do intervalo especificado único ([^-f]) ou definir ([^ abcdef]).  <br/> | *WHERE au_lname como ' de [^ l] %'* todos originar sobrenomes começando com de e onde a letra a seguir não é l.  <br/> |
   
Quando você executa comparações de sequência de caracteres usando **SEMELHANTE**, todos os caracteres na cadeia de caracteres padrão são significativos. Isso inclui espaços à esquerda ou à direita. Se não for uma comparação em uma consulta retornar todas as linhas com uma cadeia de caracteres **como** 'abc' (abc seguido por um espaço simples), uma linha em que o valor da coluna que é abc (abc sem um espaço) não será retornada. No entanto, os espaços em branco à direita, na expressão ao qual o padrão é correspondido, são ignorados. Se não for uma comparação em uma consulta retornar todas as linhas com a cadeia de caracteres **como** 'abc' (abc sem um espaço), todas as linhas que começam com abc e tem zero ou mais caracteres em branco precedentes são retornadas. 
  
Se qualquer um dos argumentos não for um cadeia de caracteres do tipo de dados, ele é convertido em um tipo de dados de cadeia de caracteres, se possível.
  

