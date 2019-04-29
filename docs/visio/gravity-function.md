---
title: Função GRAVITY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Calcula o ângulo de rotação correto de um bloco de texto para a rotação de formas indicada para evitar que o texto seja virado de cabeça para baixo.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429282"
---
# <a name="gravity-function"></a>Função GRAVITY

Calcula o ângulo de rotação correto de um bloco de texto para a rotação de formas indicada para evitar que o texto seja virado de cabeça para baixo.
  
## <a name="syntax"></a>Sintaxe

Gravidade (* * *Angle* * *, [* * *limites1* * *], [* * *limit2* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _ângulo_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | O ângulo da forma.  <br/> |
| _limites1_ <br/> |Opcional  <br/> |**String** <br/> |Primeiro limite de rotação. O padrão é 90 graus.  <br/> |
| _limit2_ <br/> |Opcional  <br/> |**String** <br/> |Segundo limite de rotação. O padrão é de 270 graus.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

A função GRAVITY é normalmente usada na célula TxtAngle. 
  
O valor retornado será 180 graus se _Angle_ estiver entre os valores especificados por _limites1_ e _limit2_; caso contrário, o valor retornado será 0 grau.
  
Todos os argumentos são automaticamente normalizados entre 0 e 360 graus pela função. Se um argumento não especificar unidades, são adotados radianos. 
  
## <a name="example-1"></a>Exemplo 1

GRAVIDADE (angular)
  
Retorna 180 graus se o *ângulo* estiver entre 90 e 270 graus; caso contrário, retornará 0 graus. 
  
## <a name="example-2"></a>Exemplo 2

GRAVIDADE (2)
  
Retorna 180 graus, porque 2 radianos fica entre 90 e 270 graus.
  
## <a name="example-3"></a>Exemplo 3

GRAVITY(100 graus, 110 graus, 290 graus)
  
Retorna 0 grau.
  
## <a name="example-4"></a>Exemplo 4

GRAVITY(100 graus, 290 graus, 110 graus)
  
Retorna 0 grau.
  

