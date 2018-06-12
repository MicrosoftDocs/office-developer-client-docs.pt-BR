---
title: Célula SketchLineChange (seção Propriedades do efeito adicionais)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Determina a quantidade de randomização da linha da forma da geometria da forma ao usar um efeito de esboço, como um percentual do tamanho de uma seção. Se o valor da célula SketchLineChange é definido como 0%, a geometria de linha da forma faz a correspondência de geometria da forma. Se o valor é 100%, a geometria de linha da forma não seguem a geometria da forma.
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772997"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>Célula SketchLineChange (seção Propriedades do efeito adicionais)

Determina a quantidade de randomização da linha da forma da geometria da forma ao usar um efeito de esboço, como um percentual do tamanho de uma seção. Se o valor da célula **SketchLineChange** é definido como 0%, a geometria de linha da forma faz a correspondência de geometria da forma. Se o valor é 100%, a geometria de linha da forma não seguem a geometria da forma. 
  
## <a name="remarks"></a>Coment�rios

Para obter melhores resultados, o intervalo de valores para a célula **SketchLineChange** ideal está entre 15% e 50%. Um valor abaixo de 15% é quase não perceptível; um valor maior do que 50% pôde tornar aleatório a linha muito grande. 
  
Para fazer referência à célula **SketchLineChange** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchLineChange  <br/> |
   
Para obter uma referência à célula **SketchLineChange** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visSketchLineChange** <br/> |
   

