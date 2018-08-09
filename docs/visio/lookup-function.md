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
description: Retorna um índice baseado em zero que indica a localização da chave subcadeia de caracteres em uma lista ou retorna -1 se a cadeia de caracteres de destino contenha o delimitador.
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772292"
---
# <a name="lookup-function"></a>Função LOOKUP

Retorna um índice baseado em zero que indica a localização da subsequência _chave_ em uma _lista_ou retorna -1 se a cadeia de caracteres de destino contenha o _delimitador_.
  
## <a name="syntax"></a>Sintaxe

PESQUISA ("* * *chave* * *","* * *lista* * *"[,"* * *delimitador* * *"]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _chave_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres que você deseja procurar.  <br/> |
| _lista_ <br/> |Obrigatório  <br/> |**String** <br/> | A lista na qual deseja fazer a pesquisa.  <br/> |
| _delimitador_ <br/> |Opcional  <br/> |**String** <br/> | A cadeia de caracteres a ser usado como um delimitador na _lista_. Uma cadeia de caracteres de _delimitador_ pode ser a mais de um caractere de comprimento e pode incluir caracteres multibyte. O padrão é um ponto e vírgula.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Numérico
  
## <a name="remarks"></a>Comentários

A função LOOKUP utiliza uma pesquisa sem fazer diferenciação entre maiúsculas e minúsculas. Se a lista começar ou terminar com um delimitador, presume-se a existência de uma sequência de caracteres nula antes ou depois da lista. Delimitadores consecutivos implicam uma sequência de caracteres nula entre eles. 
  
Todos os argumentos devem ser cadeias de caracteres ou expressões que podem ser convertidas em cadeias de caracteres. Caso contrário, uma cadeia de caracteres vazia substituirá o argumento errado. 
  
## <a name="example-1"></a>Exemplo 1

LOOKUP("rato","gato;rato;;bode")
  
Retornará 1.
  
## <a name="example-2"></a>Exemplo 2

LOOKUP("",";gato;rato;;bode")
  
Retornará 0.
  
## <a name="example-3"></a>Exemplo 3

LOOKUP("t","gato;rato;;bode","a")
  
Retornará 3.
  

