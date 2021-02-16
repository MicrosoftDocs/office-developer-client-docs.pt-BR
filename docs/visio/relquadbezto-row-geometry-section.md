---
title: Linha RelQuadBezTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier quadrática relativa à largura e altura da forma e às coordenadas x e y do ponto de controle da largura e altura da forma relativa da curva.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423353"
---
# <a name="relquadbezto-row-geometry-section"></a>Linha RelQuadBezTo (Seção Geometry)

Contém as coordenadas  *x*  e  *y*  do ponto de extremidade de uma curva de Bézier quadrática relativa à largura e altura da forma e às coordenadas  *x*  e  *y*  do ponto de controle da largura e altura da forma relativa da curva. 
  
> [!NOTE]
> Uma **linha RelQuadBezTo** só pode ser persistente nos formatos de arquivo .vsdx, .vsdm, .vstx, .vstm, .vssx e .vssm. Quando um arquivo é salvo nos formatos Visio 2003-2010, a linha **RelQuadBezTo** é convertida em uma [linha NURBSTo.](nurbsto-row-geometry-section.md) 
  
Uma **linha RelQuadBezTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A  *coordenada x*  do vértice final de uma curva de Bézier quadrática relativa à largura da forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A  *coordenada y*  do vértice final de uma curva de Bézier quadrática relativa à altura da forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A  *coordenada x*  do ponto de controle da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado aproximadamente no meio dos vértices inicial e final do arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |A  *coordenada y*  do ponto de controle de uma curva em relação à altura da forma.  <br/> |
   

