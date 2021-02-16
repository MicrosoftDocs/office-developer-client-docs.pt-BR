---
title: Célula FillGradientEnabled (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Determina se um gradiente de preenchimento está habilitado para essa forma.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431208"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>Célula FillGradientEnabled (Seção Gradient Properties)

Determina se um gradiente de preenchimento está habilitado para essa forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O preenchimento de gradiente é exibido na forma.  <br/> |
|FALSE  <br/> |Os preenchimentos de gradiente não são exibidos na forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **FillGradientEnabled** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FillGradientEnabled  <br/> |
   
Para fazer referência à célula **FillGradientEnabled** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice de célula:  <br/> |**visFillGradientEnabled ** <br/> |
   

