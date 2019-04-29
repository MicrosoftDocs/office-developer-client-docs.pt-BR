---
title: Célula SketchLineChange (seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Determina a quantidade de randomização da linha da forma a partir da geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção. Se o valor da célula SketchLineChange for definido como 0%, a geometria da linha da forma corresponderá à geometria da forma. Se o valor for 100%, a geometria da linha da forma não seguirá a geometria da forma.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419503"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>Célula SketchLineChange (seção Additional Effect Properties)

Determina a quantidade de randomização da linha da forma a partir da geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção. Se o valor da célula **SketchLineChange** for definido como 0%, a geometria da linha da forma corresponderá à geometria da forma. Se o valor for 100%, a geometria da linha da forma não seguirá a geometria da forma. 
  
## <a name="remarks"></a>Comentários

Para obter melhores resultados, o intervalo ideal de valores para a célula **SketchLineChange** está entre 15% e 50%. Um valor abaixo de 15% é mal perceptível; um valor maior do que 50% pode tornar a linha excessiva demais. 
  
Para obter uma referência para a célula **SketchLineChange** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchLineChange  <br/> |
   
Para obter uma referência para a célula **SketchLineChange** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visSketchLineChange** <br/> |
   

