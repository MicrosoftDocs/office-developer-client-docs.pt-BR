---
title: Célula QuickStyleFillColor (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Determina qual cor do tema que usa o preenchimento de uma forma, como um inteiro de 0 a 7
ms.openlocfilehash: dcbb974947821327e7cff6634fd9435f5e5845bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772630"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>Célula QuickStyleFillColor (Seção Quick Style)

Determina qual cor do tema que usa o preenchimento de uma forma, como um inteiro de 0 a 7
  
|||
|:-----|:-----|
|Value  <br/> |Descrição  <br/> |
|0  <br/> |Herda a cor do tema escuro a cor de preenchimento da forma.  <br/> |
|1  <br/> |A cor de preenchimento da forma herda a cor do tema claro.  <br/> |
|2  <br/> |A cor de preenchimento da forma herda a cor do tema Ênfase 1  <br/> |
|3  <br/> |A cor de preenchimento da forma herda a cor do tema Ênfase 2  <br/> |
|4  <br/> |A cor de preenchimento da forma herda a cor do tema Ênfase 3  <br/> |
|5  <br/> |A cor de preenchimento da forma herda a cor do tema Ênfase 4  <br/> |
|6  <br/> |A cor de preenchimento da forma herda a cor do tema Ênfase 5  <br/> |
|7  <br/> |A cor de preenchimento da forma herda a cor do tema Ênfase 6  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **QuickStyleFillColor** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | QuickStyleFillColor  <br/> |
   
Para obter uma referência à célula **QuickStyleFillColor** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice da célula:  <br/> |**visQuickStyleFillColor** <br/> |
   

