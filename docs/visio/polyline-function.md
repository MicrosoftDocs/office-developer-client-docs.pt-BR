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
description: Retorna uma polilinha. Essa função é usada na célula A de linhas geométricas de poliLinhato.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426293"
---
# <a name="polyline-function"></a>Função POLYLINE

Retorna uma polilinha. Essa função é usada na célula A de linhas geométricas de poliLinhato. 
  
## <a name="syntax"></a>Sintaxe

POLYLINE (* * *xType* * *, * * *yType* * *, * * *X1* * *, * * *Y1* * *...) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Especifica como interpretar os dados de entrada _x_ . Se _xType_ for 0, os dados de entrada _x_serão interpretados como uma porcentagem de largura. Se _xType_ for 1, os dados _x_-Input serão interpretados como uma coordenada local.  <br/> |
| _yType_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Especifica como interpretar os dados de entrada _y_. Se _yType_ for 0, os dados _y_de entrada serão interpretados como uma porcentagem da altura. Se _yType_ for 1, os dados _y_de entrada serão interpretados como uma coordenada local.  <br/> |
| _X1_ <br/> |Obrigatório  <br/> |**Número** <br/> | Uma coordenada _x_.  <br/> |
| _a1_ <br/> |Obrigatório  <br/> |**Número** <br/> |Uma coordenada _y_.  <br/> |
   
## <a name="remarks"></a>Comentários

Para cada argumento *x* , deve haver um argumento *y* ; caso contrário, um erro será retornado. 
  
## <a name="example"></a>Exemplo

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Retornará um retângulo de dimensões usando Width x Height. 
  

