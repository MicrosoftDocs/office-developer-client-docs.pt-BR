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
ms.openlocfilehash: e5725d461a71dad4623161d99134a20250abe724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425026"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>Célula ShapeRouteStyle (Seção Shape Layout)

Determina o estilo de roteamento e a direção de um conector selecionado na página de desenho.
  
|**Valor**|**Estilo de roteamento**|**Direção**|**Constante de automação**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Utilizar padrão de página  <br/> |Nenhum  <br/> |**visLORouteDefault** <br/> |
|1   <br/> |Ângulo direito  <br/> |Nenhum  <br/> |**visLORouteRightAngle** <br/> |
|2   <br/> |Reto  <br/> |Nenhum  <br/> |**visLORouteStraight** <br/> |
|3   <br/> |Organograma  <br/> |De cima para baixo  <br/> |**visLORouteOrgChartNS** <br/> |
|4   <br/> |Organograma  <br/> |Da esquerda para a direita  <br/> |**visLORouteOrgChartWE** <br/> |
|5   <br/> |Fluxograma  <br/> |De cima para baixo  <br/> |**visLORouteFlowchartNS** <br/> |
|6   <br/> |Fluxograma  <br/> |Da esquerda para a direita  <br/> |**visLORouteFlowchartWE** <br/> |
|7   <br/> |Árvore  <br/> |De cima para baixo  <br/> |**visLORouteTreeNS** <br/> |
|8   <br/> |Árvore  <br/> |Da esquerda para a direita  <br/> |**visLORouteTreeWE** <br/> |
|9   <br/> |Rede  <br/> |Nenhum  <br/> |**visLORouteNetwork** <br/> |
|10   <br/> |Organograma  <br/> |De baixo para cima  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Organograma  <br/> |Da direita para a esquerda  <br/> |**visLORouteOrgChartEW** <br/> |
|12   <br/> |Fluxograma  <br/> |De baixo para cima  <br/> |**visLORouteFlowchartSN** <br/> |
|13   <br/> |Fluxograma  <br/> |Da direita para a esquerda  <br/> |**visLORouteFlowchartEW** <br/> |
|14   <br/> |Árvore  <br/> |De baixo para cima  <br/> |**visLORouteTreeSN** <br/> |
|15   <br/> |Árvore  <br/> |Da direita para a esquerda  <br/> |**visLORouteTreeEW** <br/> |
|16   <br/> |De centro a centro  <br/> |Nenhum  <br/> |**visLORouteCenterToCenter** <br/> |
|17   <br/> |Simples  <br/> |De cima para baixo  <br/> |**visLORouteSimpleNS** <br/> |
|18   <br/> |Simples  <br/> |Da esquerda para a direita  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Simples  <br/> |De baixo para cima  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |Simples  <br/> |Da direita para a esquerda  <br/> |**visLORouteSimpleEW** <br/> |
| 21   <br/> |Horizontal-vertical simples  <br/> |Nenhum  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Vertical-horizontal simples  <br/> |Nenhum  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula para um  conector específico na guia Conector  na [](run-in-developer-mode-display-the-developer-tab.md) caixa de diálogo Comportamento  (com um conector selecionado, clique em Comportamento na guia Desenvolvedor e na guia Conector).  
  
Para definir esse comportamento para  *todos os*  conectores em uma página, use a célula RouteStyle na seção Page Layout. 
  
Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjBehavior, na seção Miscellaneous, para definir esse comportamento.
  
Para obter uma referência para a célula ShapeRouteStyle pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapeRouteStyle  <br/> |
   
Para obter uma referência para a célula ShapeRouteStyle pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice de célula:  <br/> |**visSLORouteStyle** <br/> |
   

