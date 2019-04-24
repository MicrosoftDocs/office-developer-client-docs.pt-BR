---
title: Célula PagesX (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: Determina o número de páginas impressas nas quais será ajustada horizontalmente a página de desenho.
ms.openlocfilehash: e912aef2277f5a7d2af5352897654ee986836c48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340135"
---
# <a name="pagesx-cell-print-properties-section"></a>Célula PagesX (Seção Print Properties)

Determina o número de páginas impressas nas quais será ajustada horizontalmente a página de desenho. 
  
## <a name="remarks"></a>Comentários

Esse valor é usado somente quando a célula OnPage está definida como VERDADEIRO. 
  
Para fazer referência à célula PagesX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PagesX  <br/> |
   
Para fazer referência à célula PagesX pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesPagesX** <br/> |
   

