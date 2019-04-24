---
title: Célula SketchFillChange (seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Determina a quantidade de randomização do preenchimento da forma na geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção. Se o valor da célula SketchFillChange for definido como 0%, a geometria de limite do preenchimento de uma forma corresponderá à geometria da forma. Se o valor for 100%, a geometria de limite do preenchimento da forma não seguirá a geometria da forma.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339806"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>Célula SketchFillChange (seção Additional Effect Properties)

Determina a quantidade de randomização do preenchimento da forma na geometria da forma ao usar um efeito de esboço, como uma porcentagem do comprimento de uma seção. Se o valor da célula **SketchFillChange** for definido como 0%, a geometria de limite do preenchimento de uma forma corresponderá à geometria da forma. Se o valor for 100%, a geometria de limite do preenchimento da forma não seguirá a geometria da forma. 
  
## <a name="remarks"></a>Comentários

Para obter melhores resultados, o intervalo ideal de valores para a célula **SketchFillChange** está entre 15% e 50%. Um valor abaixo de 15% é mal perceptível; um valor maior do que 50% é cada vez mais aleatório. 
  
Para obter uma referência para a célula **SketchFillChange** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchFillChange  <br/> |
   
Para obter uma referência para a célula **SketchFillChange** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visSketchFillChange** <br/> |
   

