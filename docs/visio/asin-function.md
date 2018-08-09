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
description: Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é um número.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771300"
---
# <a name="asin-function"></a>Função ASIN

Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é um *número* . 
  
## <a name="syntax"></a>Sintaxe

ASIN (* * *número* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O seno do ângulo.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor de entrada deve estar no intervalo -1 < = *número* < = 1 ou um #NUM! erro será retornado. O ângulo resultante está no intervalo -PI/2 < = *ângulo* < = PI/2 radianos (-90 < = *ângulo* < = 90 graus). 
  
## <a name="example"></a>Exemplo

ASIN(1)
  
Retorna 90 graus
  

