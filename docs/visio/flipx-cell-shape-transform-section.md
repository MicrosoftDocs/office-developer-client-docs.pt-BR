---
title: Célula FlipX (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: Indica se a forma foi virada horizontalmente.
ms.openlocfilehash: fc014ff6c5a3650361d6afd478a5858f84fb5c47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771904"
---
# <a name="flipx-cell-shape-transform-section"></a>Célula FlipX (Seção Shape Transform)

Indica se a forma foi virada horizontalmente.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A forma foi virada horizontalmente.  <br/> |
| FALSO  <br/> | A forma não foi virada horizontalmente.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula FlipX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FlipX  <br/> |
   
Para fazer referência à célula FlipX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowXFormOut** <br/> |
| Índice da célula:  <br/> |**visXFormFlipX** <br/> |
   

