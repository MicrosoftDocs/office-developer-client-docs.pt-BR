---
title: Célula KeepTextFlat (Seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indica se o texto de uma forma ignorará a rotação da forma em 3D. Não se aplica à rotação 2D.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422037"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>Célula KeepTextFlat (Seção 3-D Rotation Properties)

Indica se o texto de uma forma ignorará a rotação da forma em 3D. Não se aplica à rotação 2D. 
  
****

|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O texto da forma não gira com a geometria da forma.  <br/> |
|FALSE  <br/> |O texto da forma é transformado para girar com a geometria da forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **KeepTextFlat** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |KeepTextFlat  <br/> |
   
Para fazer referência à célula **KeepTextFlat** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice de célula:  <br/> |**visKeepTextFlat** <br/> |
   

