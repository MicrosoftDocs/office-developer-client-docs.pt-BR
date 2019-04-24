---
title: Célula RouteStyle (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251662
localization_priority: Normal
ms.assetid: 3a223dac-538b-cb5d-a32d-61395276f9da
description: Determina o estilo de roteamento e a direção para todos os conectores na página de desenho que não têm um estilo de roteamento local.
ms.openlocfilehash: 38de871460c155ee5d495599a239ebeb0ff1c33d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358440"
---
# <a name="routestyle-cell-page-layout-section"></a>Célula RouteStyle (Seção Page Layout)

Determina o estilo de roteamento e a direção para todos os conectores na página de desenho que não têm um estilo de roteamento local.
  
|**Valor**|**Estilo de roteamento**|**Direction**|**Constante de automação**|
|:-----|:-----|:-----|:-----|
|,0  <br/> |Padrão; ângulo direito  <br/> |Nenhum  <br/> |**visLORouteDefault** <br/> |
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

Você também pode definir o valor dessa célula na guia **layout e roteamento** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** , em **layout e direcionamento**e em espaçamento). **** 
  
Você pode definir um estilo de roteamento local para o conector na célula ShapeRouteStyle da seção Page Layout. 
  
Para obter uma referência à célula RouteStyle pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |RouteStyle  <br/> |
   
Para obter uma referência à célula RouteStyle pelo índice, de um programa, use a propriedade de **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLORouteStyle** <br/> |
   

