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
description: Retorna a coordenada y (no sistema de coordenadas local) do ponto onde duas linhas se cruzam.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426097"
---
# <a name="intersecty-function"></a>Função INTERSECTY

Retorna a  *coordenada y*  (no sistema de coordenadas local) do ponto onde duas linhas se cruzam. 
  
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
  
O Microsoft Visio utiliza essa função na célula PinY de uma forma colada a uma guia girada. 
  
Se as linhas não fizerem interseção, a função retornará um erro de dividido por zero (#DIV/0!), que será ignorado pelo Visio, sendo restaurado o último valor conhecido para o ponto. 
  
## <a name="example"></a>Exemplo

INTERSECTY(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Ângulo) 
  
Retorna a  *coordenada y*  do ponto de interseção de VertGuide e HorzGuide em unidades de página. 
  

