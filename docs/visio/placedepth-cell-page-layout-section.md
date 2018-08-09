---
title: Célula PlaceDepth (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Determina o tipo de layout e o método pelo qual o desenho é analisado antes de o layout ser criado.
ms.openlocfilehash: ab2c83a94c3dd03c1fdbf0c3ee187076406b2e84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772477"
---
# <a name="placedepth-cell-page-layout-section"></a>Célula PlaceDepth (Seção Page Layout)

Determina o tipo de layout e o método pelo qual o desenho é analisado antes de o layout ser criado.
  
|**Valor**|**Profundidade do deslocamento para layouts verticais e horizontais**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Padrão da página  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | Médio  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2  <br/> | Profundo  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | Raso  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula PlaceDepth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PlaceDepth  <br/> |
   
Para fazer referência à célula PlaceDepth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLOPlaceDepth** <br/> |
   

