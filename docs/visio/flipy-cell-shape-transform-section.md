---
title: Célula FlipY (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Indica se a forma foi virada verticalmente.
ms.openlocfilehash: 42ee740a13c3f447f5cd4a6caa9959189320a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771890"
---
# <a name="flipy-cell-shape-transform-section"></a>Célula FlipY (Seção Shape Transform)

Indica se a forma foi virada verticalmente.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A forma foi virada verticalmente.  <br/> |
| FALSO  <br/> | A forma não foi virada verticalmente.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula FlipY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FlipY  <br/> |
   
Para fazer referência à célula FlipY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowXFormOut** <br/> |
| Índice da célula:  <br/> |**visXFormFlipY** <br/> |
   

