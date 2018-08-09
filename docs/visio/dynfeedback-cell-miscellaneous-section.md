---
title: Célula DynFeedback (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Altera o tipo de comentário visual fornecido aos usuários ao arrastar um conector. Quando o botão do mouse é liberado, a forma do conector resultante não é afetada por essa configuração não aplicável a conectores que podem ser roteados.
ms.openlocfilehash: 858d98c8ee55eb49f58bbe98491ddc8752e75504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771790"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>Célula DynFeedback (Seção Miscellaneous)

Altera o tipo de comentário visual fornecido aos usuários ao arrastar um conector. Quando o botão do mouse é liberado, a forma do conector resultante não é afetada por essa configuração não aplicável a conectores que podem ser roteados.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Permanece reto (sem segmentos).  <br/> |**visDynFBDefault** <br/> |
| 1  <br/> | Mostra três segmentos quando arrastado.  <br/> |**visDynFBUCon3Leg** <br/> |
| 2  <br/> | Mostra cinco segmentos quando arrastado.  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula DynFeedback pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DynFeedback  <br/> |
   
Para fazer referência à célula DynFeedback pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visDynFeedback** <br/> |
   

