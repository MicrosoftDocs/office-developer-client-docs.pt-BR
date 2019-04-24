---
title: Célula ShapePlaceStyle (Seção Layout da Forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70007
localization_priority: Normal
ms.assetid: 29bfe8ec-ca12-8fbf-b62b-ece3710dfe2e
description: Especifica como as formas são colocadas na página quando as formas são colocadas na caixa de diálogo Configurar layout (na guia Design, no grupo layout, clique em reFazer o layout da página e, em seguida, clique em mais opções de layout). Armazena o estilo de layout e os valores de alinhamento do VisCellIndices.
ms.openlocfilehash: 381f74912b64395f33a2dc55c0bad24d36a16286
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326506"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>Célula ShapePlaceStyle (Seção Layout da Forma)

Especifica como as formas são colocadas na página quando as formas são colocadas na caixa de diálogo **Configurar layout** (na guia **design** , no grupo **layout** , clique em refazer o **layout da página**e, em seguida, clique em **mais opções de layout**). Armazena valores de estilo e alinhamento de layout de **VisCellIndices**. 
  
|**Constante**|**Valor**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |quatro  <br/> |
|**visLOPlaceCircular** <br/> |6  <br/> |
|**visLOPlaceCompactDownLeft** <br/> |14  <br/> |
|**visLOPlaceCompactDownRight** <br/> |178  <br/> |
|**visLOPlaceCompactLeftDown** <br/> |Treze  <br/> |
|**visLOPlaceCompactLeftUp** <br/> |3,6  <br/> |
|**visLOPlaceCompactRightDown** <br/> |8  <br/> |
|**visLOPlaceCompactRightUp** <br/> |241  <br/> |
|**visLOPlaceCompactUpLeft** <br/> |11  <br/> |
|**visLOPlaceCompactUpRight** <br/> |254  <br/> |
|**visLOPlaceDefault** <br/> |,0  <br/> |
|**visLOPlaceHierarchyBottomToTopCenter** <br/> |508  <br/> |
|**visLOPlaceHierarchyBottomToTopLeft** <br/> |19  <br/> |
|**visLOPlaceHierarchyBottomToTopRight** <br/> |21  <br/> |
|**visLOPlaceHierarchyLeftToRightBottom** <br/> |dia  <br/> |
|**visLOPlaceHierarchyLeftToRightMiddle** <br/> |23  <br/> |
|**visLOPlaceHierarchyLeftToRightTop** <br/> |22  <br/> |
|**visLOPlaceHierarchyRightToLeftBottom** <br/> |27  <br/> |
|**visLOPlaceHierarchyRightToLeftMiddle** <br/> |660  <br/> |
|**visLOPlaceHierarchyRightToLeftTop** <br/> |25  <br/> |
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |17.07.06  <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |dezesseis  <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |anos  <br/> |
|**visLOPlaceLeftToRight** <br/> |duas  <br/> |
|**visLOPlaceParentDefault** <br/> |15  <br/> |
|**visLOPlaceRadial** <br/> |3D  <br/> |
|**visLOPlaceRightToLeft** <br/> |0,5  <br/> |
|**visLOPlaceTopToBottom** <br/> |1  <br/> |
   
Para referir-se à célula ShapePlaceStyle pelo nome de outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapePlaceStyle  <br/> |
   
Para referir-se à célula ShapePlaceStyle pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOPlaceStyle** <br/> |
   

