---
title: Célula FillGradientEnabled (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Determina se um gradiente do preenchimento está habilitado para esta forma.
ms.openlocfilehash: 20a38d4c45af163bc00364a45dc31269bf97251f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771881"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>Célula FillGradientEnabled (Seção Gradient Properties)

Determina se um gradiente do preenchimento está habilitado para esta forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Preenchimento de gradiente é exibido na forma.  <br/> |
|FALSO  <br/> |Preenchimentos de gradiente não são exibidos na forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **FillGradientEnabled** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FillGradientEnabled  <br/> |
   
Para obter uma referência à célula **FillGradientEnabled** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |* * visFillGradientEnabled * * <br/> |
   

