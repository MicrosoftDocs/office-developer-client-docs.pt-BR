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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326520"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>Célula ShapeRouteStyle (Seção Shape Layout)

Determina o estilo de roteamento e a direção de um conector selecionado na página de desenho.
  
|**Valor**|**Estilo de roteamento**|**Direction**|**Constante de automação**|
|:-----|:-----|:-----|:-----|
|,0  <br/> |Utilizar padrão de página  <br/> |Nenhum  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |Ângulo direito  <br/> |Nenhum  <br/> |**visLORouteRightAngle** <br/> |
|duas  <br/> |Estreita  <br/> |Nenhum  <br/> |**visLORouteStraight** <br/> |
|3D  <br/> |Organograma  <br/> |De cima para baixo  <br/> |**visLORouteOrgChartNS** <br/> |
|quatro  <br/> |Organograma  <br/> |Da esquerda para a direita  <br/> |**visLORouteOrgChartWE** <br/> |
|0,5  <br/> |Fluxograma  <br/> |De cima para baixo  <br/> |**visLORouteFlowchartNS** <br/> |
|6  <br/> |Fluxograma  <br/> |Da esquerda para a direita  <br/> |**visLORouteFlowchartWE** <br/> |
|178  <br/> |Arvore  <br/> |De cima para baixo  <br/> |**visLORouteTreeNS** <br/> |
|8  <br/> |Arvore  <br/> |Da esquerda para a direita  <br/> |**visLORouteTreeWE** <br/> |
|241  <br/> |Rede  <br/> |Nenhum  <br/> |**visLORouteNetwork** <br/> |
|254  <br/> |Organograma  <br/> |De baixo para cima  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |Organograma  <br/> |Da direita para a esquerda  <br/> |**visLORouteOrgChartEW** <br/> |
|3,6  <br/> |Fluxograma  <br/> |De baixo para cima  <br/> |**visLORouteFlowchartSN** <br/> |
|Treze  <br/> |Fluxograma  <br/> |Da direita para a esquerda  <br/> |**visLORouteFlowchartEW** <br/> |
|14  <br/> |Arvore  <br/> |De baixo para cima  <br/> |**visLORouteTreeSN** <br/> |
|15  <br/> |Arvore  <br/> |Da direita para a esquerda  <br/> |**visLORouteTreeEW** <br/> |
|dezesseis  <br/> |De centro a centro  <br/> |Nenhum  <br/> |**visLORouteCenterToCenter** <br/> |
|17.07.06  <br/> |Simples  <br/> |De cima para baixo  <br/> |**visLORouteSimpleNS** <br/> |
|anos  <br/> |Simples  <br/> |Da esquerda para a direita  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |Simples  <br/> |De baixo para cima  <br/> |**visLORouteSimpleSN** <br/> |
|508  <br/> |Simples  <br/> |Da direita para a esquerda  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |Horizontal-vertical simples  <br/> |Nenhum  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |Vertical-horizontal simples  <br/> |Nenhum  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula para um determinado conector na guia **conector** da caixa de diálogo **comportamento** (com um conector selecionado, clique em **comportamento** na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clique na guia **conector** ). 
  
Para definir esse comportamento para *todos* os conectores em uma página, use a célula routestyle na seção Page Layout. 
  
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
   

