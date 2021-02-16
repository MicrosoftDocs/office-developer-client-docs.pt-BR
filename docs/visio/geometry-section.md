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
description: Contém linhas que listam as coordenadas das vértices para as linhas e arcos que compõem a forma.
ms.openlocfilehash: d45f960ecc697dc6f0f5a0efa18e6cbbc6e4fff0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542279"
---
# <a name="geometry-section"></a>Seção Geometry

Contém linhas que listam as coordenadas das vértices para as linhas e arcos que compõem a forma. 
  
A geometria de uma forma pode ser expressa em várias **seções Geometry.** Vários caminhos podem ser úteis quando vários caminhos têm propriedades diferentes (por exemplo, caminhos de [recorte de](clippingpath-cell-foreign-image-info-section.md) imagem). 
  
## <a name="remarks"></a>Comentários

A **seção Geometry** contém os tipos de linha a seguir. Para obter mais detalhes, consulte os tópicos sobre linhas. 
  
|Linha|Descrição|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Move para uma coordenada.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Desenha uma linha para uma coordenada.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Desenha um arco circular para uma coordenada.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Desenha um arco elíptico para uma coordenada.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Desenha uma polilinha, ou linhas consecutivas, para uma coordenada.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Desenha uma B-spline racional não uniforme (NURBS) para uma coordenada.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Inicia uma spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Desenha um segmento de spline em uma coordenada do nó.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Desenha uma linha infinita de uma coordenada para outra.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> |Desenha uma elipse a partir de uma coordenada central e um eixo principal/secundário.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Desenhar uma curva de Bezier cúbica em relação à largura e altura da forma.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Desenha um arco elíptico para uma coordenada em relação à altura e à largura da forma.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Desenha uma linha para uma coordenada relativa à altura e à largura de uma forma.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Move para uma coordenada relativa à largura e altura da forma.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Desenha uma curva de Bézier quadrática relativa à largura e altura da forma.  <br/> |
   
Para alterar um tipo de linha nesta seção, clique com o botão direito do mouse na linha e clique em **Alterar Tipo de Linha** no menu de atalho. 
  

