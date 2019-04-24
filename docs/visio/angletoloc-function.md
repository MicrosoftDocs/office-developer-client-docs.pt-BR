---
title: Função ANGLETOLOC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Retorna um ângulo transformado no sistema de coordenadas local da forma de destino. Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas locais em uma forma de destino.
ms.openlocfilehash: 804faeb24932e414ad03bc9e8487c62ca08bd7d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341472"
---
# <a name="angletoloc-function"></a>Função ANGLETOLOC

Retorna um ângulo transformado no sistema de coordenadas local da forma de destino. Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas locais em uma forma de destino. 
  
## <a name="syntax"></a>Sintaxe

ANGLETOLOC (* * *srcAngle* * *, * * *srcRef* * *, * * *dstRef* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |Um ângulo no sistema de coordenadas de origem.  <br/> |
| _srcRef_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma referência a uma célula no objeto de origem, como uma forma, um grupo, uma página, entre outros.  <br/> |
| _dstRef_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência a uma célula no objeto de destino, como uma forma, um grupo, uma página, entre outros.  <br/> |
   
## <a name="remarks"></a>Comentários

Utilize a função ANGLETOLOC para definir células de ângulo locais em uma forma de um ângulo a partir de um outro espaço de coordenadas.
  
Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.
  
As coordenadas de origem e de destino devem estar na mesma página.
  

