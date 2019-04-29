---
title: Célula QuickStyleFillColor (seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Determina a cor do tema que o preenchimento de uma forma usa, como um inteiro de 0 a 7
ms.openlocfilehash: 3ace0de7e3bfc878a2101eaca3847ef079b8f919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407960"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>Célula QuickStyleFillColor (seção Quick Style)

Determina a cor do tema que o preenchimento de uma forma usa, como um inteiro de 0 a 7
  
|||
|:-----|:-----|
|Valor  <br/> |Descrição  <br/> |
|,0  <br/> |A cor de preenchimento da forma é herdeira da cor do tema escuro.  <br/> |
|1  <br/> |A cor de preenchimento da forma é herdeira da cor do tema claro.  <br/> |
|duas  <br/> |A cor de preenchimento da forma herda da cor do tema ênfase 1  <br/> |
|3D  <br/> |A cor de preenchimento da forma é herdeira da cor do tema ênfase 2  <br/> |
|4   <br/> |A cor de preenchimento da forma é herdeira da cor do tema ênfase 3  <br/> |
|5   <br/> |A cor de preenchimento da forma é herdeira da cor do tema ênfase 4  <br/> |
|6   <br/> |A cor de preenchimento da forma herda da cor do tema ênfase 5  <br/> |
|7   <br/> |A cor de preenchimento da forma é herdeira da cor do tema ênfase 6  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **QuickStyleFillColor** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | QuickStyleFillColor  <br/> |
   
Para obter uma referência para a célula **QuickStyleFillColor** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice da célula:  <br/> |**visQuickStyleFillColor** <br/> |
   

