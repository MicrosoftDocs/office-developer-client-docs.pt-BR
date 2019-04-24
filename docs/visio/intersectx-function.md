---
title: Função INTERSECTX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Retorna a coordenada x (no sistema de coordenadas locais) do ponto em que duas linhas fazem interseção.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335305"
---
# <a name="intersectx-function"></a>Função INTERSECTX

Retorna a coordenada *x* (no sistema de coordenadas locais) do ponto em que duas linhas fazem interseção. 
  
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
  
O Microsoft Visio utiliza essa função na célula PinX de uma forma colada a uma guia girada. 
  
Se as linhas não fizerem interseção, a função retornará um erro de dividido por zero (#DIV/0!), que será ignorado pelo Visio, sendo restaurado o último valor conhecido para o ponto. 
  
## <a name="example"></a>Exemplo

INTERSECTX (VertGuide! PinX, VertGuide! PinY, VertGuide! Ângulo, HorzGuide! PinX, HorzGuide! PinY, HorzGuide! Reto 
  
Retorna a coordenada *x* do ponto de interseção de VertGuide e HorzGuide em unidades de página. 
  

