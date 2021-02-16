---
title: Célula LineGradientEnabled (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Determina se um gradiente de linha está habilitado para uma linha ou borda de uma forma.
ms.openlocfilehash: 1d2b33275d26bb0c8e5550bcb7cf282c64d34544
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416374"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>Célula LineGradientEnabled (Seção Gradient Properties)

Determina se um gradiente de linha está habilitado para uma linha ou borda de uma forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O gradiente é exibido na linha ou borda de uma forma.  <br/> |
|FALSE  <br/> |Gradientes não são exibidos na linha ou borda de uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LineGradientEnabled** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LineGradientEnabled  <br/> |
   
Para fazer referência à célula **LineGradientEnabled** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice de célula:  <br/> |**visLineGradientEnabled** <br/> |
   

