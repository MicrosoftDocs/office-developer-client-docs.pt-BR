---
title: Função ATAN2
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Retorna o ângulo entre o vetor representado por x, y e a direção do eixo x. O resultado é um número na unidade de medida atual para ângulos.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436479"
---
# <a name="atan2-function"></a>Função ATAN2

Retorna o ângulo entre o vetor representado por *x, y* e a direção do eixo *x* . O resultado é um número na unidade de medida atual para ângulos. 
  
## <a name="syntax"></a>Sintaxe

ATAN2 (* * *y* * *, * * *x* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O valor _y_do ponto.  <br/> |
| _x_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O valor _x_do ponto.  <br/> |
   
## <a name="remarks"></a>Comentários

O arco tangente é medido no sentido anti-horário do eixo *x* positivo para uma linha que cruza a origem (0, 0) e o ponto representado por *x* e *y* . No Microsoft Visio, ATAN2(0,0) retornará 0. Para forçar o resultado de ATAN2 para uma medida angular diferente, utilize as funções DEG ou RAD. 
  
A função ATAN2 é a antifunção da função TAN. A função ATAN2 retorna o ângulo cujo ângulo é igual a *y* dividido por *x* . Se ATAN2 (*y, x*) representar um ângulo em um triângulo à direita, *y* será o "lado oposto" e *x* será o "lado adjacente", para que a função possa ser gravada como ATAN2 (oposto, adjacente). 
  
## <a name="example-1"></a>Exemplo 1

ATAN2 (1,25, 2,25)
  
Retorna 29,0456 graus.
  
## <a name="example-2"></a>Exemplo 2

ATAN2 (1, SQRT (3))
  
Retorna 30 graus.
  
## <a name="example-3"></a>Exemplo 3

ATAN2 (1, 1)
  
Retorna 45 graus.
  

