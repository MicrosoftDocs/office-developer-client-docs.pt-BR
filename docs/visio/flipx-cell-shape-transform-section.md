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
ms.openlocfilehash: b7a4a15e5a7759eddcda3ec391a81f14df545691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346183"
---
# <a name="flipx-cell-shape-transform-section"></a>Célula FlipX (Seção Shape Transform)

Indica se a forma foi virada horizontalmente.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | A forma foi virada horizontalmente.  <br/> |
| FALSE  <br/> | A forma não foi virada horizontalmente.  <br/> |
   
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
   

