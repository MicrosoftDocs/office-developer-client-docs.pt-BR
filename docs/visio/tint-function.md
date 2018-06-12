---
title: Função TINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifica a cor aumentando a luminosidade pelo valor (positivo ou negativo) especificado no parâmetro int.
ms.openlocfilehash: a4b15596a4742edb4f9e4746929f19d2eafe94d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773157"
---
# <a name="tint-function"></a>Função TINT

Modifica a cor aumentando a luminosidade pelo valor (positivo ou negativo) especificado no parâmetro _int_ . 
  
## <a name="syntax"></a>Sintaxe

TONALIDADE (* * *cor* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O índice de cores do Microsoft Visio ou o valor RGB da cor.  <br/> |
| _int_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O valor pelo qual a luminosidade da cor será aumentada. Pode ser positivo ou negativo.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **RGB**
  
## <a name="remarks"></a>Coment�rios

Os limites superiores e inferiores de luminosidade são 0 e 240, respectivamente. Não há nenhum limite do tamanho do inteiro, que você pode passar para o parâmetro _int_ , mas luminosidade nunca excede esses limites. 
  

