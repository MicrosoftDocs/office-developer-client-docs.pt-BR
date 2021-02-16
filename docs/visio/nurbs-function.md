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
description: Retorna uma B-spline racional não uniforme (NURBS). Esta função é usada na célula E nas linhas de geometria NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438453"
---
# <a name="nurbs-function"></a>Função NURBS

Retorna uma B-spline racional não uniforme (NURBS). Esta função é usada na célula E nas linhas de geometria NURBSTo.
  
## <a name="syntax"></a>Sintaxe

NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Obrigatório  <br/> |**cadeia de caracteres** <br/> | O último nó.  <br/> |
| _degree_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O grau da spline.  <br/> |
| _xType_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |Especifica como interpretar os dados _de entrada x._ Se  _xType_ for 0, todos  _os dados de entrada x_ serão interpretados como uma porcentagem de Width. Se  _xType_ for 1, todos  _os dados de entrada x_ serão interpretados como coordenadas locais.  <br/> |
| _yType_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |Especifica como interpretar os dados _de entrada y._ Se  _yType_ for 0, todos os  _dados de_ entrada y serão interpretados como uma porcentagem de Altura. Se  _yType_ for 1, todos os  _dados de_ entrada y serão interpretados como coordenadas locais.  <br/> |
| _x1_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada x.  <br/> |
| _y1_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada y.  <br/> |
| _knot1_ <br/> |Obrigatório  <br/> |**String** <br/> |Um nó na B-spline.  <br/> |
| _weight1_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma espessura na B-spline.  <br/> |
   
## <a name="remarks"></a>Comentários

Para cada  *argumento x,*  deve haver um  *argumento y;*  caso contrário, um erro será retornado. 
  
Você deve especificar pelo menos um  *argumento x*, *y*, *nó*  *e*  peso; caso contrário, o Visio retornará um erro. 
  

