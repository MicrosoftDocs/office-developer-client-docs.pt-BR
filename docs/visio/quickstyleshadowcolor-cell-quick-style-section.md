---
title: Célula QuickStyleShadowColor (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0a80959f-941f-451c-9049-dc661ff4930f
description: Determina a cor do tema que a sombra de uma forma usa, como um inteiro de 0 a 7.
ms.openlocfilehash: b623eee89d214bade2706b12fcb344eccd8814b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414953"
---
# <a name="quickstyleshadowcolor-cell-quick-style-section"></a>Célula QuickStyleShadowColor (Seção Quick Style)

Determina a cor do tema que a sombra de uma forma usa, como um inteiro de 0 a 7.
  
|||
|:-----|:-----|
|Valor  <br/> |Descrição  <br/> |
|0  <br/> |A cor da sombra da forma é herdada da cor do tema Escuro.  <br/> |
|1   <br/> |A cor da sombra da forma é herdada da cor do tema Claro.  <br/> |
|2   <br/> |A cor de sombra da forma é herdada da cor do tema Ênfase 1.  <br/> |
|3   <br/> |A cor de sombra da forma é herdada da cor do tema Ênfase 2.  <br/> |
|4   <br/> |A cor de sombra da forma é herdada da cor do tema Ênfase 3.  <br/> |
|5   <br/> |A cor de sombra da forma é herdada da cor do tema Ênfase 4.  <br/> |
|6   <br/> |A cor de sombra da forma é herdada da cor do tema Ênfase 5.  <br/> |
|7   <br/> |A cor de sombra da forma é herdada da cor do tema Ênfase 6.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **QuickStyleShadowColor** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | QuickStyleShadowColor  <br/> |
   
Para fazer referência à **célula QuickStyleShadowColor** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice de célula:  <br/> |**visQuickStyleShadowColor** <br/> |
   

