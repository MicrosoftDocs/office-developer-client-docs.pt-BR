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
description: Calcula a ângulo correto do bloco de texto de rotação para a rotação da forma indicado impedir que o texto desativando cabeça para baixo.
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19771979"
---
# <a name="gravity-function"></a>Função GRAVITY

Calcula a ângulo correto do bloco de texto de rotação para a rotação da forma indicado impedir que o texto desativando cabeça para baixo.
  
## <a name="syntax"></a>Sintaxe

GRAVITY (* * *ângulo* * *, [* * *limit1* * *], [* * *limit2* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _ângulo_ <br/> |Obrigatório  <br/> |**String** <br/> | O ângulo da forma.  <br/> |
| _limit1_ <br/> |Opcional  <br/> |**String** <br/> |O padrão é de 90 graus.  <br/> |
| _limit2_ <br/> |Opcional  <br/> |**String** <br/> |Segundo limite de rotação. O padrão é de 270 graus.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

A função GRAVITY é normalmente usada na célula TxtAngle. 
  
O valor retornado será de 180 graus se o _angle_ estiver entre os valores especificados por _limit1_ e _limit2_; Caso contrário, o valor retornado será 0 grau.
  
Todos os argumentos são automaticamente normalizados entre 0 e 360 graus pela função. Se um argumento não especificar unidades, são adotados radianos. 
  
## <a name="example-1"></a>Exemplo 1

GRAVITY(Ângulo)
  
Retorna 180 graus se o *angle* estiver entre 90 e 270 graus; Caso contrário, retornará 0 grau. 
  
## <a name="example-2"></a>Exemplo 2

GRAVITY(2)
  
Retorna 180 graus, porque 2 radianos fica entre 90 e 270 graus.
  
## <a name="example-3"></a>Exemplo 3

GRAVITY(100 graus, 110 graus, 290 graus)
  
Retorna 0 grau.
  
## <a name="example-4"></a>Exemplo 4

GRAVITY(100 graus, 290 graus, 110 graus)
  
Retorna 0 grau.
  

