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
description: Retorna a coordenada x (no sistema de coordenadas local) do ponto onde duas linhas se cruzam.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418271"
---
# <a name="intersectx-function"></a>Função INTERSECTX

Retorna a  *coordenada x*  (no sistema de coordenadas local) do ponto onde duas linhas se cruzam. 
  
## <a name="syntax"></a>Sintaxe

INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Obrigatório  <br/> |**Número** <br/> |A  _coordenada x_ de um ponto na primeira linha.  <br/> |
| _y1_ <br/> |Obrigatório  <br/> |**Número** <br/> |A  _coordenada y_ de um ponto na primeira linha.  <br/> |
| _angle1_ <br/> |Obrigatório  <br/> |**Número** <br/> | O valor da célula Angle da primeira linha.  <br/> |
| _x2_ <br/> |Obrigatório  <br/> |**Número** <br/> |A  _coordenada x_ de um ponto na segunda linha.  <br/> |
| _y2_ <br/> |Obrigatório  <br/> |**Número** <br/> |A  _coordenada y_ de um ponto na segunda linha.  <br/> |
| _angle2_ <br/> |Obrigatório  <br/> |**Número** <br/> |O valor da célula Angle da segunda linha.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

Cada linha é definida como um ponto (*x,y*) e um ângulo. 
  
O Microsoft Visio utiliza essa função na célula PinX de uma forma colada a uma guia girada. 
  
Se as linhas não fizerem interseção, a função retornará um erro de dividido por zero (#DIV/0!), que será ignorado pelo Visio, sendo restaurado o último valor conhecido para o ponto. 
  
## <a name="example"></a>Exemplo

INTERSECTX(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Ângulo) 
  
Retorna a  *coordenada x*  do ponto de interseção de VertGuide e HorzGuide em unidades de página. 
  

