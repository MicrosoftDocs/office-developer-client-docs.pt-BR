---
title: Célula ShapeRouteStyle (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm905
localization_priority: Normal
ms.assetid: a5dcd2e0-e343-5ee2-2b63-2a1312437901
description: Determina o estilo de roteamento e a direção de um conector selecionado na página de desenho.
ms.openlocfilehash: b165d43e64842565806d93d620ddbd24f41a2d57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772902"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>Célula ShapeRouteStyle (Seção Shape Layout)

Determina o estilo de roteamento e a direção de um conector selecionado na página de desenho.
  
|**Valor**|**Estilo de roteamento**|**Direction**|**Constante de automação**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Utilizar padrão de página  <br/> |Nenhum  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Ângulo direito  <br/> |Nenhuma  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |Reto  <br/> |Nenhuma  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |Organograma  <br/> |De cima para baixo  <br/> |**visLORouteOrgChartNS** <br/> |
|4  <br/> |Organograma  <br/> |Da esquerda para a direita  <br/> |**visLORouteOrgChartWE** <br/> |
|5  <br/> |Fluxograma  <br/> |De cima para baixo  <br/> |**visLORouteFlowchartNS** <br/> |
|6  <br/> |Fluxograma  <br/> |Da esquerda para a direita  <br/> |**visLORouteFlowchartWE** <br/> |
|7  <br/> |Árvore  <br/> |De cima para baixo  <br/> |**visLORouteTreeNS** <br/> |
|8  <br/> |Árvore  <br/> |Da esquerda para a direita  <br/> |**visLORouteTreeWE** <br/> |
|9  <br/> |Rede  <br/> |Nenhuma  <br/> |**visLORouteNetwork** <br/> |
|10  <br/> |Organograma  <br/> |De baixo para cima  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Organograma  <br/> |Da direita para a esquerda  <br/> |**visLORouteOrgChartEW** <br/> |
|12  <br/> |Fluxograma  <br/> |De baixo para cima  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |Fluxograma  <br/> |Da direita para a esquerda  <br/> |**visLORouteFlowchartEW** <br/> |
|14  <br/> |Árvore  <br/> |De baixo para cima  <br/> |**visLORouteTreeSN** <br/> |
|15  <br/> |Árvore  <br/> |Da direita para a esquerda  <br/> |**visLORouteTreeEW** <br/> |
|16  <br/> |De centro a centro  <br/> |Nenhuma  <br/> |**visLORouteCenterToCenter** <br/> |
|17  <br/> |Simples  <br/> |De cima para baixo  <br/> |**visLORouteSimpleNS** <br/> |
|18  <br/> |Simples  <br/> |Da esquerda para a direita  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Simples  <br/> |De baixo para cima  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Simples  <br/> |Da direita para a esquerda  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Horizontal-vertical simples  <br/> |Nenhuma  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Vertical-horizontal simples  <br/> |Nenhuma  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula para um determinado conector na guia **conector** na caixa de diálogo **comportamento** (com um conector selecionado, clique em **comportamento** , na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clique na guia **conector** ). 
  
Para definir esse comportamento para *todos* os conectores em uma página, use a célula RouteStyle na seção Page Layout. 
  
Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjBehavior, na seção Miscellaneous, para definir esse comportamento.
  
Para obter uma referência para a célula ShapeRouteStyle pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapeRouteStyle  <br/> |
   
Para obter uma referência para a célula ShapeRouteStyle pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLORouteStyle** <br/> |
   

