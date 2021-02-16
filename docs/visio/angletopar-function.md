---
title: Função ANGLETOPAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Retorna um ângulo transformado no sistema de coordenadas pai da forma de destino. Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas pai em uma forma de destino.
ms.openlocfilehash: 0fed51e264bfb21da25d4e91f20f4bc0803e46e8
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160255"
---
# <a name="angletopar-function"></a>Função ANGLETOPAR

Retorna um ângulo transformado no sistema de coordenadas pai da forma de destino. Converte um ângulo de coordenadas locais em uma forma de origem para as coordenadas pai em uma forma de destino. 
  
## <a name="syntax"></a>Sintaxe

ANGLETOPAR(***srcAngle***, ***srcRef***, ***dstRef*** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |Um ângulo no sistema de coordenadas de origem.  <br/> |
| _srcRef_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma referência a uma célula no objeto de origem, como uma forma, um grupo, uma página, entre outros.  <br/> |
| _dstRef_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência a uma célula no objeto de destino, como uma forma, um grupo, uma página, entre outros.  <br/> |
   
## <a name="remarks"></a>Comentários

Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.
  
As coordenadas de origem e de destino devem estar na mesma página.
  
Se o destino for uma página que não tem um pai, o resultado será expresso em coordenadas locais da página.
  

