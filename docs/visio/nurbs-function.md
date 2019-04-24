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
description: Retorna uma B-spline racional não-uniforme (NURBS). Essa função é usada na célula E nas linhas de geometria NURBSto.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340121"
---
# <a name="nurbs-function"></a>Função NURBS

Retorna uma B-spline racional não-uniforme (NURBS). Essa função é usada na célula E nas linhas de geometria NURBSto.
  
## <a name="syntax"></a>Sintaxe

NURBS (* * *knotLast* * *, * * *grau* * *, * * *xType* * *, * * *yType* * *, * * *X1* * *, * * *Y1* * *, * * *knot1* * *, * * ** [* *,...) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Obrigatório  <br/> |**cadeia de caracteres** <br/> | O último nó.  <br/> |
| _alto_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O grau da spline.  <br/> |
| _xType_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |Especifica como interpretar os dados de entrada _x_ . Se _xType_ for 0, todos os dados de entrada _x_ serão interpretados como uma porcentagem de largura. Se _xType_ for 1, todos os dados de entrada _x_ serão interpretados como coordenadas locais.  <br/> |
| _yType_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |Especifica como interpretar os dados de entrada de _y_ . Se _yType_ for 0, todos os dados de entrada de _y_ serão interpretados como uma porcentagem de Height. Se _yType_ for 1, todos os dados de entrada de _y_ serão interpretados como coordenadas locais.  <br/> |
| _X1_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada x.  <br/> |
| _a1_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada y.  <br/> |
| _knot1_ <br/> |Obrigatório  <br/> |**String** <br/> |Um nó na B-spline.  <br/> |
| _weight1_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma espessura na B-spline.  <br/> |
   
## <a name="remarks"></a>Comentários

Para cada argumento *x* , deve haver um argumento *y* ; caso contrário, um erro será retornado. 
  
É necessário especificar pelo menos um argumento *x*, *y*, *nó* e *Weight* ; caso contrário, o Visio retornará um erro. 
  

