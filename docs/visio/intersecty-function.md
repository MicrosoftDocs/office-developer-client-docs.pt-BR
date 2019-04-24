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
description: Retorna a coordenada y (no sistema de coordenadas locais) do ponto em que duas linhas fazem interseção.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335256"
---
# <a name="intersecty-function"></a>Função INTERSECTY

Retorna a coordenada *y* (no sistema de coordenadas locais) do ponto em que duas linhas fazem interseção. 
  
## <a name="syntax"></a>Sintaxe

INTERSECTX (* * *X1* * *, * * *Y1* * *, * * *angle1* * *, * * *X2* * *, * * *Y2* * *, * * *angle2* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _X1_ <br/> |Obrigatório  <br/> |**Número** <br/> |A coordenada _x_de um ponto na primeira linha.  <br/> |
| _a1_ <br/> |Obrigatório  <br/> |**Número** <br/> |A coordenada _y_de um ponto na primeira linha.  <br/> |
| _angle1_ <br/> |Obrigatório  <br/> |**Número** <br/> | O valor da célula Angle da primeira linha.  <br/> |
| _X2_ <br/> |Obrigatório  <br/> |**Número** <br/> |A coordenada _x_de um ponto na segunda linha.  <br/> |
| _Y2_ <br/> |Obrigatório  <br/> |**Número** <br/> |A coordenada _y_de um ponto na segunda linha.  <br/> |
| _angle2_ <br/> |Obrigatório  <br/> |**Número** <br/> |O valor da célula Angle da segunda linha.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

Cada linha é definida como um ponto (*x,y*) e um ângulo. 
  
O Microsoft Visio utiliza essa função na célula PinY de uma forma colada a uma guia girada. 
  
Se as linhas não fizerem interseção, a função retornará um erro de dividido por zero (#DIV/0!), que será ignorado pelo Visio, sendo restaurado o último valor conhecido para o ponto. 
  
## <a name="example"></a>Exemplo

INTERSECT (VertGuide! PinX, VertGuide! PinY, VertGuide! Ângulo, HorzGuide! PinX, HorzGuide! PinY, HorzGuide! Reto 
  
Retorna a coordenada *y* do ponto de interseção de VertGuide e HorzGuide em unidades de página. 
  

