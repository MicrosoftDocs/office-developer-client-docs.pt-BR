---
title: Célula SketchFillChange (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina a quantidade de randomização do preenchimento da forma a partir da geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção. Se o valor da célula SketchFillChange for definido como 0%, a geometria delimitada do preenchimento de uma forma corresponde à geometria da forma. Se o valor for 100%, a geometria delimitada do preenchimento da forma não seguirá a geometria da forma.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408072"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>Célula SketchFillChange (Seção Additional Effect Properties)

Determina a quantidade de randomização do preenchimento da forma a partir da geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção. Se o valor da célula **SketchFillChange** for definido como 0%, a geometria delimitada do preenchimento de uma forma corresponde à geometria da forma. Se o valor for 100%, a geometria delimitada do preenchimento da forma não seguirá a geometria da forma. 
  
## <a name="remarks"></a>Comentários

Para melhores resultados, o intervalo ideal de valores para a célula **SketchFillChange** é entre 15% e 50%. Um valor abaixo de 15% é perceptível; um valor maior que 50% é cada vez mais aleatório. 
  
Para fazer referência à célula **SketchFillChange** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchFillChange  <br/> |
   
Para fazer referência à célula **SketchFillChange** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de célula:  <br/> |**visSketchFillChange** <br/> |
   

