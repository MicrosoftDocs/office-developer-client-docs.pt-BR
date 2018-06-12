---
title: Função SHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica a cor reduzindo a luminosidade pelo valor (positivo ou negativo) especificado no parâmetro int.
ms.openlocfilehash: 4a02aa41050c3cf36b567c238670b5f61074bd7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772871"
---
# <a name="shade-function"></a>Função SHADE

Modifica a cor reduzindo a luminosidade pelo valor (positivo ou negativo) especificado no parâmetro _int_ . 
  
## <a name="syntax"></a>Sintaxe

SOMBREAMENTO (* * *cor* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O índice de cores do Microsoft Visio ou o valor RGB da cor.  <br/> |
| _int_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O valor pelo qual a luminosidade da cor será reduzida. Pode ser positivo ou negativo.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **RGB**
  
## <a name="remarks"></a>Coment�rios

Os limites superiores e inferiores de luminosidade são 0 e 240, respectivamente. Não há nenhum limite do tamanho do inteiro, que você pode passar para o parâmetro _int_ , mas luminosidade nunca excede esses limites. 
  
![](media/image199_ZA10173627.gif)
  

