---
title: Célula SketchAmount (seção Additional Effect Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Determina a quantidade de distorção para um efeito de esboço, como um inteiro entre 0 e 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314767"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>Célula SketchAmount (seção Additional Effect Properties)

Determina a quantidade de distorção para um efeito de esboço, como um inteiro entre 0 e 25. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |A forma não tem efeito de esboço aplicado a ela.  <br/> |
|1-25  <br/> |A forma tem distorção de esboço aplicada a ela, onde um valor de 1 é a maior distorção e 25 é o menos.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **SketchAmount** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SketchAmount  <br/> |
   
Para obter uma referência para a célula **SketchAmount** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowOtherEffectProperties** <br/> |
| Índice da célula:  <br/> |**visSketchAmount** <br/> |
   

