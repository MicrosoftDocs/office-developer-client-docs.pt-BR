---
title: Célula Rotationtype (seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina se a forma segue uma rotação paralela, uma rotação de perspectiva ou uma rotação oblíqua, como um inteiro de 0 a 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315670"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>Célula Rotationtype (seção 3-D Rotation Properties)

Determina se a forma segue uma rotação paralela, uma rotação de perspectiva ou uma rotação oblíqua, como um inteiro de 0 a 6. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |A forma não tem nenhuma rotação.  <br/> |
|1  <br/> |A forma tem uma rotação paralela.  <br/> |
|duas  <br/> |A forma tem uma rotação em perspectiva.  <br/> |
|3D  <br/> |A forma tem uma rotação oblíquo superior esquerda.  <br/> |
|quatro  <br/> |A forma tem uma rotação oblíqua para a direita superior.  <br/> |
|0,5  <br/> |A forma tem uma rotação oblíquo inferior à esquerda.  <br/> |
|6  <br/> |A forma tem uma rotação oblíqua inferior à direita.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a **** célula rotationtype pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |RotationType  <br/> |
   
Para obter uma referência para a **** célula rotationtype pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice da célula:  <br/> |**visRotationType** <br/> |
   

