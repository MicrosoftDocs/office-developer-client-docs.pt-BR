---
title: Célula PagesY (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Determina o número de páginas impressas nas quais será ajustada verticalmente a página de desenho.
ms.openlocfilehash: 43d4081439525c516d3da28b6c0e46e9273d85c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339974"
---
# <a name="pagesy-cell-print-properties-section"></a>Célula PagesY (Seção Print Properties)

Determina o número de páginas impressas nas quais será ajustada verticalmente a página de desenho. 
  
## <a name="remarks"></a>Comentários

Esse valor é usado somente quando a célula OnPage está definida como VERDADEIRO. 
  
Para fazer referência à célula PagesY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PagesY  <br/> |
   
Para fazer referência à célula PagesY pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesPagesY** <br/> |
   

