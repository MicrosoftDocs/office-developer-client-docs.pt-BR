---
title: Função INTERSECTY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Retorna a y-coordenada (no sistema de coordenadas locais) do ponto de interseção de duas linhas.
ms.openlocfilehash: c3c0e9afef317ed4c647f1d236c4c3a29c6cdaa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772083"
---
# <a name="intersecty-function"></a>Função INTERSECTY

Retorna a *y* -coordenada (no sistema de coordenadas locais) do ponto de interseção de duas linhas. 
  
## <a name="syntax"></a>Sintaxe

INTERSECTX (* * *x1* * *, * * *y1* * *, * * *angle1* * *, * * *x2* * *, * * *y2* * *, * * *angle2* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Obrigatório  <br/> |**Número** <br/> |_X_-coordenadas de um ponto na primeira linha.  <br/> |
| _Y1_ <br/> |Obrigatório  <br/> |**Número** <br/> |_Y_-coordenadas de um ponto na primeira linha.  <br/> |
| _angle1_ <br/> |Obrigatório  <br/> |**Número** <br/> | O valor da célula Angle da primeira linha.  <br/> |
| _X2_ <br/> |Obrigatório  <br/> |**Número** <br/> |_X_-coordenadas de um ponto na segunda linha.  <br/> |
| _a2_ <br/> |Obrigatório  <br/> |**Número** <br/> |_Y_-coordenadas de um ponto na segunda linha.  <br/> |
| _angle2_ <br/> |Obrigatório  <br/> |**Número** <br/> |O valor da célula Angle da segunda linha.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Number
  
## <a name="remarks"></a>Comentários

Cada linha é definida como um ponto (*x,y*) e um ângulo. 
  
O Microsoft Visio utiliza essa função na célula PinY de uma forma colada a uma guia girada. 
  
Se as linhas não fizerem interseção, a função retornará um erro de dividido por zero (#DIV/0!), que será ignorado pelo Visio, sendo restaurado o último valor conhecido para o ponto. 
  
## <a name="example"></a>Exemplo

INTERSECTY (VertGuide! PinX, VertGuide! PinY, VertGuide! Ângulo, HorzGuide! PinX, HorzGuide! PinY, HorzGuide! Ângulo) 
  
Retorna a *y* -coordenadas do ponto de interseção de VertGuide e HorzGuide em unidades de página. 
  

