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
description: Retorna o ângulo entre o vetor representado por x, y e a direção da x-eixo. O resultado é um número na unidade atual de medida para ângulos.
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771264"
---
# <a name="atan2-function"></a>Função ATAN2

Retorna o ângulo entre o vetor representado por *x, y* e a direção da *x* -eixo. O resultado é um número na unidade atual de medida para ângulos. 
  
## <a name="syntax"></a>Sintaxe

ATAN2 (* * *y* * *, * * *x* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |_Y_-valor do ponto.  <br/> |
| _x_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |_X_-o valor do ponto.  <br/> |
   
## <a name="remarks"></a>Comentários

O arco tangente é o ângulo medido no sentido anti-horário do positivo *x* -eixo para uma linha que intercepta a origem (0,0) e o ponto representado por *x* e *y* . No Microsoft Visio, ATAN2(0,0) retornará 0. Para forçar o resultado de ATAN2 para uma medida angular diferente, use as funções DEG ou RAD. 
  
A função ATAN2 é a antifunção da função TAN. A função ATAN2 retorna o ângulo cujo ângulo é igual a *y* dividido por *x* . Se ATAN2 (*y, x*) representando um ângulo no triângulo, *y* é o "lado oposto" e *x* é o "lado adjacente", portanto, a função poderia ser gravada como ATAN2. 
  
## <a name="example-1"></a>Exemplo 1

ATAN2(1.25,2.25)
  
Retorna 29,0456 graus.
  
## <a name="example-2"></a>Exemplo 2

ATAN2(1,SQRT(3))
  
Retorna 30 graus.
  
## <a name="example-3"></a>Exemplo 3

ATAN2(1,1)
  
Retorna 45 graus.
  

