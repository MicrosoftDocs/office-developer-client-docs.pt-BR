---
title: Célula ConLineJumpStyle (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: Determina o estilo de saltos de linha em um conector dinâmico.
ms.openlocfilehash: d3e27ddb6689fb5635674b3c4a8462fe587bce7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771586"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>Célula ConLineJumpStyle (Seção Shape Layout)

Determina o estilo de saltos de linha em um conector dinâmico.
  
|**Valor**|**Estilo de salto de linha**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Padrão da página  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arco  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Intervalo  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Quadrado  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |Triangle  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 lados  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 lados  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 lados  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 lados  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 lados  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>Comentários

Você pode também definir o valor desta célula selecionando um conector dinâmico, clicando em **comportamento** , no grupo **Design** da forma na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **conector** . 
  
Para obter uma referência para a célula ConLineJumpStyle pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ConLineJumpStyle  <br/> |
   
Para obter uma referência para a célula ConLineJumpStyle pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  

