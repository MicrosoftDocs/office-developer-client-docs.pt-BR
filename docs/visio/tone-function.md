---
title: Função TONE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifica a cor reduzindo sua saturação pelo valor especificado no parâmetro int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335683"
---
# <a name="tone-function"></a>Função TONE

Modifica a cor reduzindo sua saturação pelo valor especificado no parâmetro _int_ . 
  
## <a name="syntax"></a>Sintaxe

Tom (* * *cor* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O índice de cores do Microsoft Visio ou o valor RGB da cor.  <br/> |
| _int_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O valor pelo qual a saturação da cor será reduzida. Pode ser positivo ou negativo.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **RGB**
  
## <a name="remarks"></a>Comentários

Os limites superior e inferior de saturação são, respectivamente, 0 e 240. Não há limite para o tamanho do inteiro que você pode passar para o parâmetro _int_ , mas a saturação nunca excede esses limites. 
  

