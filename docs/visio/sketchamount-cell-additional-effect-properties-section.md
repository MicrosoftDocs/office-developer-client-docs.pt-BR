---
title: Célula SketchAmount (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Determina a quantidade de distorção para um efeito de esboço, como um número inteiro entre 0 e 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772994"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>Célula SketchAmount (Seção Additional Effect Properties)

Determina a quantidade de distorção para um efeito de esboço, como um número inteiro entre 0 e 25. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |A forma não tem nenhum efeito de esboço aplicado a ela.  <br/> |
|1-25  <br/> |A forma não tiver aplicada a ele, onde um valor de 1 é a maioria das distorção e é de 25 de distorção de esboço a menos.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **SketchAmount** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchAmount  <br/> |
   
Para obter uma referência à célula **SketchAmount** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visSketchAmount** <br/> |
   

