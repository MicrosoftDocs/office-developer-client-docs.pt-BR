---
title: Função BLEND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Combina duas cores na proporção especificada pelo parâmetro float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432783"
---
# <a name="blend-function"></a>Função BLEND

Combina duas cores na proporção especificada pelo parâmetro _float._ 
  
## <a name="syntax"></a>Sintaxe

BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O índice de cores do Visio ou o valor RGB da primeira cor.  <br/> |
| _color2_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O índice de cores do Visio ou o valor RGB da segunda cor.  <br/> |
| _float[0,1]_ <br/> |Obrigatório  <br/> |**Float** <br/> |A proporção na qual mesclar  _color2_ e  _color1,_ respectivamente. Um número real de 0 a 1.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **RGB**
  
## <a name="remarks"></a>Comentários

A cor retornada é determinada pelas proporções relativas nas quais a _cor2_ e _color1_ são mescladas, respectivamente, conforme especificado pelo parâmetro _float._ Por exemplo, se  _float_ for 0,25, a cor retornada será composta por 75% da  _cor1_ e 25% da  _cor2_. 
  
Outra maneira de pensar sobre  isso é que o valor flutuante corresponde ao ponto ao longo do espectro de cores de _color1_ a _color2_. Portanto, números menores (mais próximos de zero) para  _float_ produzem combinações mais próximas da  _cor1,_ enquanto números maiores (mais próximos de 1) produzem combinações mais próximas  _da cor2_.
  

