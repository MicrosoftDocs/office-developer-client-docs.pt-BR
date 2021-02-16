---
title: Função SHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica a cor diminuindo sua luminosidade pela quantidade (positiva ou negativa) especificada no parâmetro int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326591"
---
# <a name="shade-function"></a>Função SHADE

Modifica a cor diminuindo sua luminosidade pela quantidade (positiva ou negativa) especificada no _parâmetro int._ 
  
## <a name="syntax"></a>Sintaxe

SHADE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O índice de cores do Microsoft Visio ou o valor RGB da cor.  <br/> |
| _int_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O valor pelo qual a luminosidade da cor será reduzida. Pode ser positivo ou negativo.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **RGB**
  
## <a name="remarks"></a>Comentários

Os limites superior e inferior de luminosidade são, respectivamente, 0 e 240. Não há limite para o tamanho do inteiro que você pode passar para o parâmetro  _int,_ mas a luminosidade nunca excede esses limites. 
  
![Limites superiores e inferiores de luminosidade](media/image199_ZA10173627.gif)
  

