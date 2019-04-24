---
title: Linha RelCubBezTo (seção geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contém as coordenadas x e y do ponto de extremidade de uma curva Bézier cúbica em relação à largura e à altura da forma, as coordenadas x e y do ponto de controle do início da largura e altura da forma relativa da curva e as coordenadas x e y do contro ponto l do final da largura e altura da forma relativa da curva.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320031"
---
# <a name="relcubbezto-row-geometry-section"></a>Linha RelCubBezTo (seção geometry)

Contém as coordenadas *x* e *y* do ponto de extremidade de uma curva Bézier cúbica em relação à largura e altura da forma, as coordenadas *x* e *y* do ponto de controle do início da largura e altura da forma relativa da curva. e as coordenadas *x* e *y* do ponto de controle do fim da largura e altura da forma relativa da curva. 
  
> [!NOTE]
> Uma linha **RelCubBezTo** só pode persistir nos formatos de arquivo. vsdx,. vsdm,. vstx,. VSTM,. vssx e. vssm. Quando um arquivo é salvo nos formatos do Visio 2003-2010, a linha **RelCubBezTo** é convertida em uma linha [nurbsto](nurbsto-row-geometry-section.md) . 
  
Uma linha **RelCubBezTo** contém as células a seguir. 
  
|**Cell**|**Descrição**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |A coordenada *x* do vértice final de uma curva Bézier cúbica em relação à largura da forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |A coordenada *y* do vértice final de uma curva Bézier cúbica em relação à altura da forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |A coordenada *x* do ponto de controle inicial da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado entre os vértices inicial e final do arco.  <br/> |
|[A.b.c.](b-cell-geometry-section.md) <br/> |A coordenada *y* do ponto de controle inicial de uma curva em relação à altura da forma.  <br/> |
|[Unidade](c-cell-geometry-section.md) <br/> |A coordenada *x* do ponto de controle final da curva em relação à largura da forma; um ponto no arco. O ponto de controle é melhor localizado entre o ponto de controle inicial e os vértices finais do arco.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |A coordenada *y* do ponto de controle final de uma curva em relação à altura da forma.  <br/> |
   

