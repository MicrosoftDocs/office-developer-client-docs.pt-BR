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
description: Retorna a subcadeia de caracteres no índice de local baseado em zero na lista delimitada por delimitador. Ou, se o índice estiver fora do intervalo, retorna uma cadeia de caracteres vazia ou o token opcional fornecido como o argumento errorvalue.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431572"
---
# <a name="index-function"></a>Função INDEX

Retorna a subcadeia de caracteres no _índice_ de local baseado em zero na _lista_ delimitada __ por delimitador. Ou, se o índice estiver fora do intervalo, retorna uma cadeia de caracteres vazia ou o token opcional fornecido ** como o argumento errorvalue. 
  
## <a name="syntax"></a>Sintaxe

Index (* * *index* * *, "* * *list* * *" [, [* * ** delimitador * *] [, [* * *errorvalue* * *]]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _índice_ <br/> |Obrigatório  <br/> |**Número** <br/> |A localização que deseja encontrar.  <br/> |
| _list_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A lista na qual deseja fazer a pesquisa.  <br/> |
| _delimitador_ <br/> |Opcional  <br/> |**String** <br/> | A cadeia de caracteres a ser usada como um delimitador na _lista_. Uma __ cadeia de caracteres de delimitador pode ter mais de um caractere e incluir caracteres multibyte. O padrão é um ponto-e-vírgula.  <br/> |
| _errorvalue_ <br/> |Opcional  <br/> |**Número** <br/> | Um valor especificado pelo usuário para retornar se o índice estiver fora do intervalo. O padrão é uma cadeia de caracteres vazia.  <br/> |
   
## <a name="remarks"></a>Comentários

Se a lista começar ou terminar com um delimitador, presume-se a existência de uma sequência de caracteres nula antes ou depois da lista. Delimitadores consecutivos implicam uma sequência de caracteres nula entre eles. 
  
Se o índice estiver fora do intervalo, o Visio retornará uma cadeia de caracteres vazia ou o token opcional ** fornecido como o argumento errorvalue. 
  
## <a name="example-1"></a>Exemplo 1

ÍNDICE (3, "gato; Rat;; bode ")
  
Retornará "bode".
  
## <a name="example-2"></a>Exemplo 2

ÍNDICE (54, "; 1; 2; 3;",, "ERRO")
  
Retorna "erro".
  

