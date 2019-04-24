---
title: Célula LineGradientEnabled (seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Determina se um gradiente de linha está habilitado para uma linha ou borda de uma forma.
ms.openlocfilehash: 1d2b33275d26bb0c8e5550bcb7cf282c64d34544
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361135"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>Célula LineGradientEnabled (seção Gradient Properties)

Determina se um gradiente de linha está habilitado para uma linha ou borda de uma forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |Gradiente é exibido na linha ou borda de uma forma.  <br/> |
|FALSE  <br/> |Gradientes não são exibidos na linha ou borda de uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **LineGradientEnabled** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LineGradientEnabled  <br/> |
   
Para obter uma referência para a célula **LineGradientEnabled** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |**visLineGradientEnabled** <br/> |
   

