---
title: Célula BeginArrow (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Indica se a linha tem uma ponta de seta ou outro formato de fim de linha em seu primeiro vértice. Insira um número de 0 a 45, utilize a função USE com o nome de um fim de linha personalizado ou use a caixa de diálogo Linha.
ms.openlocfilehash: c6d5a66d76cfea61b1c9923c5b904dadec5495f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771287"
---
# <a name="beginarrow-cell-line-format-section"></a>Célula BeginArrow (Seção Line Format)

Indica se a linha tem uma ponta de seta ou outro formato de fim de linha em seu primeiro vértice. Insira um número de 0 a 45, utilize a função USE com o nome de um fim de linha personalizado ou use a caixa de diálogo **Linha**. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| 0  <br/> | Sem ponta de seta.  <br/> |
| 1 - 45  <br/> | Estilos de ponta de seta variados correspondentes a entradas indexadas na caixa de diálogo **Linha**.  <br/> |
   
## <a name="remarks"></a>Comentários

O tamanho da ponta de seta é definido na célula BeginArrowSize.
  
Para fazer referência à célula BeginArrow pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | BeginArrow  <br/> |
   
Para fazer referência à célula BeginArrow pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLine** <br/> |
| Índice da célula:  <br/> |**visLineBeginArrow** <br/> |
   

