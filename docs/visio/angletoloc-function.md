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
ms.openlocfilehash: e971613d4fc33cd991e7e9aeba49ac47871ebe8f
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160262"
---
# <a name="angletoloc-function"></a>Função ANGLETOLOC

Retorna um ângulo transformado no sistema de coordenadas local da forma de destino. Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas locais em uma forma de destino. 
  
## <a name="syntax"></a>Sintaxe

ANGLETOLOC (***srcAngle***, ***srcRef***, ***dstRef*** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |Um ângulo no sistema de coordenadas de origem.  <br/> |
| _srcRef_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma referência a uma célula no objeto de origem, como uma forma, um grupo, uma página, entre outros.  <br/> |
| _dstRef_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência a uma célula no objeto de destino, como uma forma, um grupo, uma página, entre outros.  <br/> |
   
## <a name="remarks"></a>Comentários

Utilize a função ANGLETOLOC para definir células de ângulo locais em uma forma de um ângulo a partir de um outro espaço de coordenadas.
  
Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.
  
As coordenadas de origem e de destino devem estar na mesma página.
  

