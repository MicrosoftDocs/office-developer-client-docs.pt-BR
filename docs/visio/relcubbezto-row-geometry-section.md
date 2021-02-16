---
title: Linha RelCubBezTo (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contém as coordenadas x e y do ponto de extremidade de uma curva de Bézier cúbica relativas à largura e altura da forma, às coordenadas x e y do ponto de controle do início da largura e altura da forma relativa da curva e as coordenadas x - e y -do ponto de controle do final da largura e altura da forma relativa da curva.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430326"
---
# <a name="relcubbezto-row-geometry-section"></a>Linha RelCubBezTo (Seção Geometry)

Contém as coordenadas  *x*  e  *y*  do ponto de extremidade de uma curva de Bézier cúbica relativas à largura e altura da forma, às coordenadas  *x*  e  *y*  do ponto de controle do início da largura e altura da forma relativa da curva e as coordenadas  *x*  - e  *y -do*  ponto de controle do final da largura e altura da forma relativa da curva. 
  
> [!NOTE]
> Uma **linha RelCubBezTo** só pode ser persistente nos formatos de arquivo .vsdx, .vsdm, .vstx, .vstm, .vssx e .vssm. Quando um arquivo é salvo nos formatos Visio 2003-2010, a linha **RelCubBezTo** é convertida em uma [linha NURBSTo.](nurbsto-row-geometry-section.md) 
  
Uma **linha RelCubBezTo** contém as células a seguir. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A  *coordenada x*  do vértice final de uma curva de Bézier cúbica relativa à largura da forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A  *coordenada y*  do vértice final de uma curva de Bézier cúbica relativa à altura da forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A  *coordenada x*  do ponto de controle inicial da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado entre os vértices inicial e final do arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |A  *coordenada y*  do ponto de controle inicial de uma curva em relação à altura da forma.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |A  *coordenada x*  do ponto de controle final da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado entre o ponto de controle inicial e os vértices finais do arco.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |A  *coordenada y*  do ponto de controle final de uma curva em relação à altura da forma.  <br/> |
   

