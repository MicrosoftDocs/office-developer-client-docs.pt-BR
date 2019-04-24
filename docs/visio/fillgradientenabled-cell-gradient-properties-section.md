---
title: Célula FillGradientEnabled (seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Determina se um gradiente de preenchimento está habilitado para esta forma.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322488"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>Célula FillGradientEnabled (seção Gradient Properties)

Determina se um gradiente de preenchimento está habilitado para esta forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |O preenchimento gradual é exibido na forma.  <br/> |
|FALSE  <br/> |Os preenchimentos de gradiente não são exibidos na forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **FillGradientEnabled** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FillGradientEnabled  <br/> |
   
Para obter uma referência para a célula **FillGradientEnabled** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |* * visFillGradientEnabled * * <br/> |
   

