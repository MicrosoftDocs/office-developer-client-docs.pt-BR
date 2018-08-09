---
title: Célula SketchLineWeight (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Determina a espessura adicional adicionada a espessura da linha como o resultado de um efeito de esboço, em pontos de 0 a 50. A espessura da linha de uma forma aumenta à medida que o valor do SketchLineWeight célula aumenta.
ms.openlocfilehash: 9ab99faab907ddf0d944abbeea39672906b4c03d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773014"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a>Célula SketchLineWeight (Seção Additional Effect Properties)

Determina a espessura adicional adicionada a espessura da linha como o resultado de um efeito de esboço, em pontos de 0 a 50. A espessura da linha de uma forma aumenta à medida que o valor do **SketchLineWeight** célula aumenta. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula **SketchLineWeight** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchLineWeight  <br/> |
   
Para obter uma referência à célula **SketchLineWeight** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visSketchLineWeight** <br/> |
   

