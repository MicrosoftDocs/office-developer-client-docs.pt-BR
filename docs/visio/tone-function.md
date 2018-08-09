---
title: Função TONE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifica a cor diminuindo sua saturação pelo valor especificado no parâmetro int.
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773167"
---
# <a name="tone-function"></a>Função TONE

Modifica a cor diminuindo sua saturação pelo valor especificado no parâmetro _int_ . 
  
## <a name="syntax"></a>Sintaxe

TOM (* * *cor* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O índice de cores do Microsoft Visio ou o valor RGB da cor.  <br/> |
| _int_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O valor pelo qual a saturação da cor será reduzida. Pode ser positivo ou negativo.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **RGB**
  
## <a name="remarks"></a>Comentários

Os limites superiores e inferiores de saturação são 0 e 240, respectivamente. Não há nenhum limite do tamanho do inteiro, que você pode passar para o parâmetro _int_ , mas saturação nunca excede esses limites. 
  

