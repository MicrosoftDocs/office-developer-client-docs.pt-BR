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
ms.openlocfilehash: d64e7b3c7cf30f0a657ede57b227acefd4b10101
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772764"
---
# <a name="routestyle-cell-page-layout-section"></a>Célula RouteStyle (Seção Page Layout)

Determina o estilo de roteamento e a direção para todos os conectores na página de desenho que não têm um estilo de roteamento local.
  
|**Valor**|**Estilo de roteamento**|**Direction**|**Constante de automação**|
|:-----|:-----|:-----|:-----|
|0  <br/> |Padrão; ângulo direito  <br/> |Nenhuma  <br/> |**visLORouteDefault** <br/> |
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

Você também pode definir o valor dessa célula na guia **Layout e roteamento** na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** , clique em **Layout e roteamento**e clique em **espaçamento** ). 
  
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
   

