---
title: Célula SketchSeed (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Representa um valor de randomização usado para determinar a geometria de um efeito de esboço, como um inteiro positivo. O valor da célula SketchSeed é criado aleatoriamente quando um efeito de esboço é aplicado à forma.
ms.openlocfilehash: 3ec58fbfa183d1a6d7bb6960672658f9a6cca073
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434393"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>Célula SketchSeed (Seção Additional Effect Properties)

Representa um valor de randomização usado para determinar a geometria de um efeito de esboço, como um inteiro positivo. O valor da célula **SketchSeed** é criado aleatoriamente quando um efeito de esboço é aplicado à forma. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula **SketchSeed** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchSeed  <br/> |
   
Para fazer referência à célula **SketchSeed** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de célula:  <br/> |**visSketchSeed** <br/> |
   

