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
ms.openlocfilehash: 44ea0341cda3655e8acc69e82e89acddac69b80d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417445"
---
# <a name="flipy-cell-shape-transform-section"></a>Célula FlipY (Seção Shape Transform)

Indica se a forma foi virada verticalmente.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A forma foi virada verticalmente.  <br/> |
| FALSE  <br/> | A forma não foi virada verticalmente.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula FlipY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FlipY  <br/> |
   
Para fazer referência à célula FlipY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowXFormOut** <br/> |
| Índice da célula:  <br/> |**visXFormFlipY** <br/> |
   

