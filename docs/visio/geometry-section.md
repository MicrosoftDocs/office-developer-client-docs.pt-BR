---
title: Seção Geometry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Contém linhas que listam as coordenadas dos vértices de linhas e arcos que compõem a forma.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771954"
---
# <a name="geometry-section"></a>Seção Geometry

Contém linhas que listam as coordenadas dos vértices de linhas e arcos que compõem a forma. 
  
A geometria de uma forma pode ser expressa em várias seções **Geometry** . Vários caminhos podem ser útil quando vários caminhos tem propriedades diferentes (por exemplo, caminhos de [recorte de imagem](clippingpath-cell-foreign-image-info-section.md) ). 
  
## <a name="remarks"></a>Comentários

A seção **Geometry** contém os seguintes tipos de linha. Para obter detalhes, consulte os tópicos de linha. 
  
|**Row**|**Descrição**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Move para uma coordenada.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Desenha uma linha para uma coordenada.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Desenha um arco circular para uma coordenada.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Desenha um arco elíptico para uma coordenada.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Desenha uma polilinha, ou linhas consecutivas, para uma coordenada.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Desenha uma não-uniforme rational B-spline uniforme (NURBS) para uma coordenada.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Inicia uma spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Desenha um segmento de spline em uma coordenada do nó.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Desenha uma linha infinita de uma coordenada para outra.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> |Desenha uma elipse a partir de uma coordenada central e um eixo principal/secundário.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Desenhe uma curva de Bézier cúbica em relação a largura e altura da forma.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Desenha um arco elíptico para uma coordenada em relação a altura e largura da forma.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Desenha uma linha para coordenadas relativo a altura e largura de uma forma.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Move para uma coordenada em relação a largura e altura da forma.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Desenha uma curva de Bézier quadrática em relação a largura e altura da forma.  <br/> |
   
Para alterar um tipo de linha nesta seção, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho. 
  

