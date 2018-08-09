---
title: Célula LineGradientEnabled (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Determina se um gradiente de linha está habilitado para uma linha ou borda de uma forma.
ms.openlocfilehash: d78a94a25c0290bd5e58522c9a45955868f31b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772185"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>Célula LineGradientEnabled (Seção Gradient Properties)

Determina se um gradiente de linha está habilitado para uma linha ou borda de uma forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Gradiente é exibida na linha ou a borda de uma forma.  <br/> |
|FALSO  <br/> |Gradientes não são exibidas na linha ou a borda de uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LineGradientEnabled** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LineGradientEnabled  <br/> |
   
Para obter uma referência à célula **LineGradientEnabled** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |**visLineGradientEnabled** <br/> |
   

