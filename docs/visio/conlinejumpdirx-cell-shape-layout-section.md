---
title: Célula ConLineJumpDirX (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Determina a direção dos saltos de linha que ocorrem em um conector dinâmico horizontal para uma forma.
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771573"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>Célula ConLineJumpDirX (Seção Shape Layout)

Determina a direção dos saltos de linha que ocorrem em um conector dinâmico horizontal para uma forma.
  
|**Valor**|**Direção do salto de linha**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Padrão da página  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Acima  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Abaixo  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Comentários

Para definir o padrão direção horizontal para o conector de *todos os* saltos em uma página, utilize a célula PageLineJumpDirX na seção Page Layout. 
  
Para fazer referência à célula ConLineJumpDirX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ConLineJumpDirX  <br/> |
   
Para fazer referência à célula ConLineJumpDirX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
| Índice da célula:  <br/> |**visSLOJumpDirX** <br/> |
   

