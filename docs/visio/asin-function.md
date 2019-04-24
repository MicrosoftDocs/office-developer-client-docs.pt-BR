---
title: Função ASIN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é núm.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341521"
---
# <a name="asin-function"></a>Função ASIN

Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é *núm* . 
  
## <a name="syntax"></a>Sintaxe

Asen (* * *número* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O seno do ângulo.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor de entrada deve estar no intervalo-1 < = *Number* < = 1, ou um #NUM! será retornado. O ângulo resultante está no intervalo-PI/2 < = *Angle* _LT_ = pi/2 radianos (-90 < = *angle* < = 90 graus). 
  
## <a name="example"></a>Exemplo

ASEN (1)
  
Retorna 90 graus
  

