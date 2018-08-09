---
title: Célula SketchSeed (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Representa um valor de randomização usado para determinar a geometria de um efeito de esboço, como um número inteiro positivo. O valor da célula SketchSeed aleatoriamente é criado quando um efeito de esboço é aplicado à forma.
ms.openlocfilehash: 7c9d23e19da1a94bb37f1fc916e2f08095976d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773000"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>Célula SketchSeed (Seção Additional Effect Properties)

Representa um valor de randomização usado para determinar a geometria de um efeito de esboço, como um número inteiro positivo. O valor da célula **SketchSeed** aleatoriamente é criado quando um efeito de esboço é aplicado à forma. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula **SketchSeed** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchSeed  <br/> |
   
Para obter uma referência à célula **SketchSeed** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visSketchSeed** <br/> |
   

