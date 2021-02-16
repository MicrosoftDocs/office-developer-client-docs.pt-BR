---
title: Célula RotationType (Seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina se a forma segue uma rotação paralela, uma rotação de perspectiva ou uma rotação oblíqua, como um inteiro de 0 a 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422940"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>Célula RotationType (Seção 3-D Rotation Properties)

Determina se a forma segue uma rotação paralela, uma rotação de perspectiva ou uma rotação oblíqua, como um inteiro de 0 a 6. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |A forma não tem rotação.  <br/> |
|1   <br/> |A forma tem uma rotação paralela.  <br/> |
|2   <br/> |A forma tem uma rotação de perspectiva.  <br/> |
|3   <br/> |A forma tem uma rotação oblíqua superior esquerda.  <br/> |
|4   <br/> |A forma tem uma rotação oblíqua superior direita.  <br/> |
|5   <br/> |A forma tem uma rotação oblíqua inferior esquerda.  <br/> |
|6   <br/> |A forma tem uma rotação oblíqua direita inferior.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **RotationType** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |RotationType  <br/> |
   
Para fazer referência à célula **RotationType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice de célula:  <br/> |**visRotationType** <br/> |
   

