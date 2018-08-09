---
title: Função BLEND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Combina duas cores na proporção especificada pelo parâmetro float.
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771391"
---
# <a name="blend-function"></a>Função BLEND

Combina duas cores na proporção especificada pelo parâmetro _float_ . 
  
## <a name="syntax"></a>Sintaxe

MISTURA (* * *color1* * *, * * *color2* * *, * * *float [0,1]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Color1_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O índice de cores do Visio ou o valor RGB da primeira cor.  <br/> |
| _Color2_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O índice de cores do Visio ou o valor RGB da segunda cor.  <br/> |
| _float [0,1]_ <br/> |Obrigatório  <br/> |**Float** <br/> |A proporção no qual mesclar _color2_ e _color1_, respectivamente. Um número de real entre 0 e 1 inclusive.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **RGB**
  
## <a name="remarks"></a>Comentários

A cor retornada é determinada pelas proporções relativas no qual mesclar _color2_ e _color1_, respectivamente, conforme especificado pelo parâmetro _float_ . Por exemplo, se _float_ for 0,25, a cor retornada é compostas 75% das _cor1_ e 25% dos _color2_. 
  
Outra maneira de pensar sobre ele é que o valor de _float_ corresponde ao ponto ao longo do espectro de cores de _color1_ para _color2_. Portanto, menor números (mais próximo do zero) para quase misturas de produzir _float_ para _color1_, enquanto os números maior (mais perto de 1) produzem misturas quase _color2_.
  

