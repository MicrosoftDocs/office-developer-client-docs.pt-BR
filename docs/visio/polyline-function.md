---
title: Função POLYLINE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Retorna uma polilinha. Esta função é usada na célula A das linhas de geometria PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426293"
---
# <a name="polyline-function"></a>Função POLYLINE

Retorna uma polilinha. Esta função é usada na célula A das linhas de geometria PolyLineTo. 
  
## <a name="syntax"></a>Sintaxe

POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Especifica como interpretar os dados _de entrada x._ Se  _xType_ for 0, a  _entrada x_-data será interpretada como uma porcentagem de Largura. Se  _xType_ for 1, os  _dados x_ de entrada serão interpretados como uma coordenada local.  <br/> |
| _yType_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Especifica como interpretar os dados de entrada _y._ Se  _yType_ for 0, os dados  _y_ de entrada serão interpretados como uma porcentagem de Height. Se  _yType_ for 1, os dados  _y_ de entrada serão interpretados como uma coordenada local.  <br/> |
| _x1_ <br/> |Obrigatório  <br/> |**Número** <br/> | Uma _coordenada x._  <br/> |
| _y1_ <br/> |Obrigatório  <br/> |**Número** <br/> |Uma coordenada _y._  <br/> |
   
## <a name="remarks"></a>Comentários

Para cada  *argumento x,*  deve haver um  *argumento y;*  caso contrário, um erro será retornado. 
  
## <a name="example"></a>Exemplo

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Retornará um retângulo de dimensões usando Width x Height. 
  

