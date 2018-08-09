---
title: Célula KeepTextFlat Cell (Seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indica se o texto de uma forma irá ignorar a rotação da forma em 3D. Não se aplicam a rotação 2D.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772136"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>Célula KeepTextFlat Cell (Seção 3-D Rotation Properties)

Indica se o texto de uma forma irá ignorar a rotação da forma em 3D. Não se aplicam a rotação 2D. 
  
****

|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Texto da forma não gira com a geometria da forma.  <br/> |
|FALSO  <br/> |Texto da forma é transformado para girar com geometria da forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **KeepTextFlat** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |KeepTextFlat  <br/> |
   
Para obter uma referência à célula **KeepTextFlat** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice da célula:  <br/> |**visKeepTextFlat** <br/> |
   

