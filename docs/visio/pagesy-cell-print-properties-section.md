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
ms.openlocfilehash: 1663fac8efdf06599d1e3c00d5eb0d00ec52e476
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772458"
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
   

