---
title: Função NURBS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Retorna uma B-spline racional não-uniforme (NURBS). Essa função é usada na célula E nas linhas geométricas NURBSTo.
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772457"
---
# <a name="nurbs-function"></a>Função NURBS

Retorna uma B-spline racional não-uniforme (NURBS). Essa função é usada na célula E nas linhas geométricas NURBSTo.
  
## <a name="syntax"></a>Sintaxe

NURBS (* * *knotLast* * *, * * *grau* * *, * * *tipoX* * *, * * *tipoY* * *, * * *x1* * *, * * *y1* * *, * * *knot1* * *, * * *weight1* * *,...) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Obrigatório  <br/> |**cadeia de caracteres** <br/> | O último nó.  <br/> |
| _grau_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O grau da spline.  <br/> |
| _tipoX_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |Especifica como interpretar os dados de entrada de _x_ . Se _tipoX_ for 0, todos os dados de entrada _x_ será interpretada como uma porcentagem da largura. Se _tipoX_ for 1, todos os dados de entrada _x_ será interpretada como coordenadas locais.  <br/> |
| _tipoY_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |Especifica como interpretar os dados de entrada _y_ . Se _tipoY_ for 0, todos os dados de entrada _y_ será interpretada como uma porcentagem da altura. Se _tipoY_ for 1, todos os dados de entrada _y_ será interpretada como coordenadas locais.  <br/> |
| _x1_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada x.  <br/> |
| _Y1_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada y.  <br/> |
| _knot1_ <br/> |Obrigatório  <br/> |**String** <br/> |Um nó na B-spline.  <br/> |
| _weight1_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma espessura na B-spline.  <br/> |
   
## <a name="remarks"></a>Comentários

Para cada argumento *x* , deve haver um argumento *y* ; Caso contrário, um erro será retornado. 
  
Você deve especificar pelo menos um *x*, *y*, *nó* e *espessura* argumento; Caso contrário, o Visio retornará um erro. 
  

