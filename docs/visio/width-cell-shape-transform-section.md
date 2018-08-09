---
title: Célula Width (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Contém a largura da forma selecionada em unidades de desenho. A fórmula padrão para determinar a largura de uma forma 1D é:'
ms.openlocfilehash: 55e77c5ccfca2425a8a2985564448e0f656aebbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773278"
---
# <a name="width-cell-shape-transform-section"></a>Célula Width (Seção Shape Transform)

Contém a largura da forma selecionada em unidades de desenho. A fórmula padrão para determinar a largura de uma forma 1D é:
  
= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Width pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Width  <br/> |
   
Para fazer referência à célula Width pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowXFormOut** <br/> |
| Índice da célula:  <br/> |**visXFormWidth** <br/> |
   

