---
title: Célula RotationType (Seção 3-D Rotation Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina se a forma segue uma rotação paralela, rotação de uma perspectiva ou uma rotação Oblíqua, como um inteiro de 0 a 6.
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772778"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>Célula RotationType (Seção 3-D Rotation Properties)

Determina se a forma segue uma rotação paralela, rotação de uma perspectiva ou uma rotação Oblíqua, como um inteiro de 0 a 6. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |A forma não tem qualquer rotação.  <br/> |
|1  <br/> |A forma não tiver uma rotação paralela.  <br/> |
|2  <br/> |A forma não tiver uma rotação perspectiva.  <br/> |
|3  <br/> |A forma não tiver uma rotação de oblíqua superior à esquerda.  <br/> |
|4  <br/> |A forma não tiver uma rotação oblíqua à direita superior.  <br/> |
|5  <br/> |A forma não tiver uma rotação de oblíqua inferior à esquerda.  <br/> |
|6  <br/> |A forma não tiver uma parte inferior direita oblíqua rotação.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **RotationType** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |RotationType  <br/> |
   
Para obter uma referência à célula **RotationType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRow3DRotationProperties** <br/> |
|Índice da célula:  <br/> |**visRotationType** <br/> |
   

