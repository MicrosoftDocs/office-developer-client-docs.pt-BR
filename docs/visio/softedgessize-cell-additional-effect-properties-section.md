---
title: Célula SoftEdgesSize (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: Determina o tamanho de um efeito de borda suave, em pontos, de 0,00 a 100,00. Se a célula SoftEdgesSize tiver um valor 0, a forma não terá bordas suaves.
ms.openlocfilehash: e749fefde8e0358cbf4ab8388a61ad703c7d52ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435912"
---
# <a name="softedgessize-cell-additional-effect-properties-section"></a>Célula SoftEdgesSize (Seção Additional Effect Properties)

Determina o tamanho de um efeito de borda suave, em pontos, de 0,00 a 100,00. Se a **célula SoftEdgesSize** tiver um valor 0, a forma não terá bordas suaves. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula **SoftEdgesSize** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SoftEdgesSize  <br/> |
   
Para fazer referência à célula **SoftEdgesSize** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de célula:  <br/> |**visSoftEdgesSize** <br/> |
   

