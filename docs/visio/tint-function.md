---
title: Função TINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifica a cor aumentando sua luminosidade pelo valor (positivo ou negativo) especificado no parâmetro int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406574"
---
# <a name="tint-function"></a>Função TINT

Modifica a cor aumentando sua luminosidade pelo valor (positivo ou negativo) especificado no parâmetro _int_ . 
  
## <a name="syntax"></a>Sintaxe

TONALIDADE (* * *cor* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O índice de cores do Microsoft Visio ou o valor RGB da cor.  <br/> |
| _int_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O valor pelo qual a luminosidade da cor será aumentada. Pode ser positivo ou negativo.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **RGB**
  
## <a name="remarks"></a>Comentários

Os limites superior e inferior de luminosidade são, respectivamente, 0 e 240. Não há limite para o tamanho do inteiro que você pode passar para o parâmetro _int_ , mas a luminosidade nunca excede esses limites. 
  

