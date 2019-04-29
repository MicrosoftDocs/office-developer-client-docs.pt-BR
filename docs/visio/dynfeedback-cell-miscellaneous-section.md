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
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404796"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>Célula DynFeedback (Seção Miscellaneous)

Altera o tipo de comentário visual fornecido aos usuários ao arrastar um conector. Quando o botão do mouse é liberado, a forma do conector resultante não é afetada por essa configuração não aplicável a conectores que podem ser roteados.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Permanece reto (sem segmentos).  <br/> |**visDynFBDefault** <br/> |
| 1  <br/> | Mostra três segmentos quando arrastado.  <br/> |**visDynFBUCon3Leg** <br/> |
| duas  <br/> | Mostra cinco segmentos quando arrastado.  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula DynFeedback pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DynFeedback  <br/> |
   
Para fazer referência à célula DynFeedback pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowMisc** <br/> |
| Índice de célula:  <br/> |**visDynFeedback** <br/> |
   

