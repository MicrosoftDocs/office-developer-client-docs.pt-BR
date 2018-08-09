---
title: Célula SketchFillChange (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina a quantidade de randomização do preenchimento da forma da geometria da forma ao usar um efeito de esboço, como um percentual do tamanho de uma seção. Se o valor da célula SketchFillChange é definido como 0%, a geometria de contorno de preenchimento de uma forma faz a correspondência de geometria da forma. Se o valor é 100%, a geometria de contorno de preenchimento da forma não seguem a geometria da forma.
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773002"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>Célula SketchFillChange (Seção Additional Effect Properties)

Determina a quantidade de randomização do preenchimento da forma da geometria da forma ao usar um efeito de esboço, como um percentual do tamanho de uma seção. Se o valor da célula **SketchFillChange** é definido como 0%, a geometria de contorno de preenchimento de uma forma faz a correspondência de geometria da forma. Se o valor é 100%, a geometria de contorno de preenchimento da forma não seguem a geometria da forma. 
  
## <a name="remarks"></a>Comentários

Para obter melhores resultados, o intervalo de valores para a célula **SketchFillChange** ideal está entre 15% e 50%. Um valor abaixo de 15% é quase não perceptível; um valor maior do que 50% cada vez mais é aleatória. 
  
Para fazer referência à célula **SketchFillChange** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchFillChange  <br/> |
   
Para obter uma referência à célula **SketchFillChange** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visSketchFillChange** <br/> |
   

