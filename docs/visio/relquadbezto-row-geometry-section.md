---
title: Linha RelQuadBezTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contém os x e y - coordenadas do ponto de extremidade de uma curva de Bézier quadrática em relação à largura da forma e a altura e a x - e y-coordenadas do ponto de controle de largura e a altura da forma relativa curva.
ms.openlocfilehash: 99796e85a857fd320598cb48993fc29bdfa4964d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772723"
---
# <a name="relquadbezto-row-geometry-section"></a>Linha RelQuadBezTo (Seção Geometry)

Contém os *x* e *y* - coordenadas do ponto de extremidade de uma curva de Bézier quadrática em relação à largura da forma e a altura e o *x* - e *y* -coordenadas do ponto de controle de largura e a altura da forma relativa curva. 
  
> [!NOTE]
> Uma linha **RelQuadBezTo** só pode ser mantida nos formatos de arquivo. vsdx,. vsdm,. vstx,. vstm,. vssx e. vssm. Quando um arquivo é salva para os formatos de 2010 do Visio 2003, a linha **RelQuadBezTo** é convertida em uma linha [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Uma linha de **RelQuadBezTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordenadas do vértice final de uma curva de Bézier quadrática relativa à largura da forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -coordenadas do vértice final de uma curva de Bézier quadrática relativa à altura da forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -coordenadas do ponto de controle da curva em relação à largura da forma; um ponto do arco. O ponto de controle está localizado melhor sobre na metade entre exagerada vértices do arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -coordenadas do ponto de controle da curva em relação à altura da forma.  <br/> |
   

