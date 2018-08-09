---
title: Função INDEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Retorna a subcadeia de caracteres no índice baseado em zero local na lista delimitada pelo delimitador. Ou, se o índice estiver fora do intervalo, retorna uma cadeia de caracteres vazia ou o token opcional fornecido como o argumento errorvalue.
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772067"
---
# <a name="index-function"></a>Função INDEX

Retorna a subcadeia de caracteres no _índice_ baseado em zero local na _lista_ delimitada pelo _delimitador_. Ou, se o índice estiver fora do intervalo, retorna uma cadeia de caracteres vazia ou o token opcional fornecido como o argumento *errorvalue* . 
  
## <a name="syntax"></a>Sintaxe

ÍNDICE (* * *índice* * *, "* * *lista* * *" [, [* * *delimitador* * *] [, [* * *errorvalue* * *]]]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _índice_ <br/> |Obrigatório  <br/> |**Número** <br/> |A localização que deseja encontrar.  <br/> |
| _lista_ <br/> |Obrigatório  <br/> |**String** <br/> |A lista na qual deseja fazer a pesquisa.  <br/> |
| _delimitador_ <br/> |Opcional  <br/> |**String** <br/> | A cadeia de caracteres a ser usado como um delimitador na _lista_. Uma cadeia de caracteres de _delimitador_ pode ter mais de um caractere e incluir caracteres multibyte. O padrão é um ponto e vírgula.  <br/> |
| _valor de erro_ <br/> |Opcional  <br/> |**Número** <br/> | Um valor especificado pelo usuário para retornar se o índice estiver fora do intervalo. O padrão é uma cadeia de caracteres vazia.  <br/> |
   
## <a name="remarks"></a>Comentários

Se a lista começar ou terminar com um delimitador, presume-se a existência de uma sequência de caracteres nula antes ou depois da lista. Delimitadores consecutivos implicam uma sequência de caracteres nula entre eles. 
  
Se o índice estiver fora do intervalo, o Visio retornará uma cadeia de caracteres vazia ou o token opcional fornecido como o argumento *errorvalue* . 
  
## <a name="example-1"></a>Exemplo 1

INDEX(3,"gato;rato;;bode")
  
Retornará "bode".
  
## <a name="example-2"></a>Exemplo 2

INDEX(54,";1;2;3;",,"ERRO")
  
Retornará "Erro".
  

