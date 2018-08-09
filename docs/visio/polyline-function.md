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
description: Retorna uma polilinha. Essa função é usada na célula a das linhas geométricas PolyLineTo.
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772504"
---
# <a name="polyline-function"></a>Função POLYLINE

Retorna uma polilinha. Essa função é usada na célula a das linhas geométricas PolyLineTo. 
  
## <a name="syntax"></a>Sintaxe

POLILINHA (* * *tipoX* * *, * * *tipoY* * *, * * *x1* * *, * * *y1* * *...) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _tipoX_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Especifica como interpretar os dados de entrada de _x_ . Se _tipoX_ for 0, a entrada _x_-dados serão interpretadas como uma porcentagem da largura. Se _tipoX_ for 1, a entrada _x_-dados serão interpretadas como uma coordenada local.  <br/> |
| _tipoY_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Especifica como interpretar o _y_-entrada de dados. Se _tipoY_ for 0, a entrada _y_-dados serão interpretadas como uma porcentagem da altura. Se _tipoY_ for 1, a entrada _y_-dados serão interpretadas como uma coordenada local.  <br/> |
| _x1_ <br/> |Obrigatório  <br/> |**Número** <br/> | Um _x_-coordenar.  <br/> |
| _Y1_ <br/> |Obrigatório  <br/> |**Número** <br/> |Um _y_-coordenar.  <br/> |
   
## <a name="remarks"></a>Comentários

Para cada argumento *x* , deve haver um argumento *y* ; Caso contrário, um erro será retornado. 
  
## <a name="example"></a>Exemplo

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Retornará um retângulo de dimensões usando Width x Height. 
  

