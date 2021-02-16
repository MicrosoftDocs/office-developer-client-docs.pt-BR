---
title: Função LOOKUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Retorna um índice baseado em zero que indica o local da chave de substring em uma lista ou retorna -1 se a cadeia de caracteres de destino contiver o delimiter.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410326"
---
# <a name="lookup-function"></a>Função LOOKUP

Retorna um índice baseado em zero que indica _o_ local da chave de substring  em uma lista ou retorna -1 se a cadeia de caracteres de destino contiver o _delimiter_.
  
## <a name="syntax"></a>Sintaxe

LOOKUP(" ** *key* ** "," ** *list* ** "[," ** *delimiter* ** "]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _key_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres que você deseja procurar.  <br/> |
| _lista_ <br/> |Obrigatório  <br/> |**String** <br/> | A lista na qual deseja fazer a pesquisa.  <br/> |
| _delimitador_ <br/> |Opcional  <br/> |**String** <br/> | A cadeia de caracteres a ser usada como um delimiter dentro da _lista._ Uma  _cadeia de caracteres do delimidor_ pode ter mais de um caractere e pode incluir caracteres de váriosbyte. O padrão é um ponto-e-vírgula.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Numeric
  
## <a name="remarks"></a>Comentários

A função LOOKUP utiliza uma pesquisa sem fazer diferenciação entre maiúsculas e minúsculas. Se a lista começar ou terminar com um delimitador, presume-se a existência de uma sequência de caracteres nula antes ou depois da lista. Delimitadores consecutivos implicam uma sequência de caracteres nula entre eles. 
  
Todos os argumentos devem ser cadeias de caracteres ou expressões que podem ser convertidas em cadeias de caracteres. Caso contrário, uma cadeia de caracteres vazia substituirá o argumento errado. 
  
## <a name="example-1"></a>Exemplo 1

LOOKUP("rat","cat;rat;; ").
  
Retornará 1.
  
## <a name="example-2"></a>Exemplo 2

LOOKUP("",";cat;rat;; ").
  
Retornará 0.
  
## <a name="example-3"></a>Exemplo 3

LOOKUP("t","cat;rat;; aaa","a")
  
Retornará 3.
  

