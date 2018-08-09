---
title: Célula SoftEdgesSize (Seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: Determina o tamanho de um efeito de borda suave, em pontos, da 0,00 para 100,00. Se a célula SoftEdgesSize possuir um valor igual a 0, a forma não tenha bordas suaves.
ms.openlocfilehash: 3b301ae2e8c82867be2a486f2e93c2275fbf3914
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773030"
---
# <a name="softedgessize-cell-additional-effect-properties-section"></a>Célula SoftEdgesSize (Seção Additional Effect Properties)

Determina o tamanho de um efeito de borda suave, em pontos, da 0,00 para 100,00. Se a célula **SoftEdgesSize** possuir um valor igual a 0, a forma não tenha bordas suaves. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula **SoftEdgesSize** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SoftEdgesSize  <br/> |
   
Para obter uma referência à célula **SoftEdgesSize** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visSoftEdgesSize** <br/> |
   

