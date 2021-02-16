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
description: Retorna a substring no índice de local baseado em zero na lista delimitada pelo delimitador. Ou, se o índice estiver fora do intervalo, retornará uma cadeia de caracteres vazia ou o token opcional fornecido como o argumento errorvalue.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431572"
---
# <a name="index-function"></a>Função INDEX

Retorna a substring no índice  de local baseado em zero na lista _delimitada_ _pelo delimitador_. Ou, se o índice estiver fora do intervalo, retornará uma cadeia de caracteres vazia ou o token opcional fornecido como o *argumento errorvalue.* 
  
## <a name="syntax"></a>Sintaxe

INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _índice_ <br/> |Obrigatório  <br/> |**Número** <br/> |A localização que deseja encontrar.  <br/> |
| _lista_ <br/> |Obrigatório  <br/> |**String** <br/> |A lista na qual deseja fazer a pesquisa.  <br/> |
| _delimitador_ <br/> |Opcional  <br/> |**String** <br/> | A cadeia de caracteres a ser usada como um delimiter dentro da _lista._ Uma  _cadeia de caracteres do delimidor_ pode ter mais de um caractere e incluir caracteres multibyte. O padrão é um ponto-e-vírgula.  <br/> |
| _errorvalue_ <br/> |Opcional  <br/> |**Número** <br/> | Um valor especificado pelo usuário para retornar se o índice estiver fora do intervalo. O padrão é uma cadeia de caracteres vazia.  <br/> |
   
## <a name="remarks"></a>Comentários

Se a lista começar ou terminar com um delimitador, presume-se a existência de uma sequência de caracteres nula antes ou depois da lista. Delimitadores consecutivos implicam uma sequência de caracteres nula entre eles. 
  
Se o índice estiver fora do intervalo, o Visio retornará uma cadeia de caracteres vazia ou o token opcional fornecido como o *argumento errorvalue.* 
  
## <a name="example-1"></a>Exemplo 1

INDEX(3,"cat;rat;; ").
  
Retornará "bode".
  
## <a name="example-2"></a>Exemplo 2

INDEX(54,";1;2;3;",,"ERROR")
  
Retorna "ERROR".
  

