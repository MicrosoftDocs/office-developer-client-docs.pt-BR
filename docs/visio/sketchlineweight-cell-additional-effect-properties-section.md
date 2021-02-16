---
title: Célula SketchLineWeight (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Determina a espessura adicional adicionada à espessura da linha como resultado de um efeito de esboço, em pontos de 0 a 50. A espessura da linha de uma forma aumenta à medida que o valor da célula SketchLineWeight aumenta.
ms.openlocfilehash: 0ee71bbaec59f5c79b72314b08478f8028b4e0ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404509"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a>Célula SketchLineWeight (Seção Additional Effect Properties)

Determina a espessura adicional adicionada à espessura da linha como resultado de um efeito de esboço, em pontos de 0 a 50. A espessura da linha de uma forma aumenta à medida que o valor da célula **SketchLineWeight** aumenta. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula **SketchLineWeight** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchLineWeight  <br/> |
   
Para fazer referência à célula **SketchLineWeight** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice de célula:  <br/> |**visSketchLineWeight** <br/> |
   

