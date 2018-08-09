---
title: Linha RelCubBezTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contém x - e y - coordenadas do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, x - e y - coordenadas do ponto de controle do início da largura da forma relativa curva e altura e o x - e y-coordenadas do contro l ponto do final da largura e a altura da forma relativa curva.
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772675"
---
# <a name="relcubbezto-row-geometry-section"></a>Linha RelCubBezTo (Seção Geometry)

Contém os *x* e *y* - coordenadas do ponto de extremidade de uma curva de Bézier cúbica em relação à largura da forma e a altura, *x* - e *y* -coordenadas do ponto de controle do início da largura e a altura da forma relativa curva e o *x* e *y* -coordenadas do ponto de controle do final da largura e a altura da forma relativa curva. 
  
> [!NOTE]
> Uma linha **RelCubBezTo** só pode ser mantida nos formatos de arquivo. vsdx,. vsdm,. vstx,. vstm,. vssx e. vssm. Quando um arquivo é salva para os formatos de 2010 do Visio 2003, a linha **RelCubBezTo** é convertida em uma linha [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Uma linha de **RelCubBezTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordenadas do vértice final de uma curva de Bézier cúbica relativa à largura da forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -coordenadas do vértice final de uma curva de Bézier cúbica relativa à altura da forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -coordenadas da curva inicial do ponto de controle em relação à largura da forma; um ponto do arco. O ponto de controle é melhor localizado entre o início e fim vértices do arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |*Y* -coordenadas de uma curva inicial do ponto de controle em relação à altura da forma.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X* -coordenadas da curva final do ponto de controle em relação à largura da forma; um ponto do arco. O ponto de controle é melhor localizado entre os vértices início de ponto de e terminando de controle do arco.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |*Y* -coordenadas de uma curva final do ponto de controle em relação à altura da forma.  <br/> |
   

