---
title: Célula FillGradientDir (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina a direção do gradiente de preenchimento. Um gradiente pode ser linear, radial, retangular ou seguir um caminho.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406714"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>Célula FillGradientDir (Seção Gradient Properties)

Determina a direção do gradiente de preenchimento. Um gradiente pode ser linear, radial, retangular ou seguir um caminho. 
  
> [!NOTE]
> Um gradiente linear é o único gradiente que recebe um valor de ângulo adicional (conforme determinado pela **célula FillGradientDir).** Todas as outras direções de gradiente têm enumerações predefinidas. 
  
****

|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Gradiente linear. A **célula FillGradientAngle** determina a direção do gradiente.  <br/> |
|1-7  <br/> |Gradientes radiales. O gradiente se estende para fora em um círculo a partir de um ponto central.  <br/> |
|8-12  <br/> |Gradientes retangulares. O gradiente se estende como uma linha direcional de uma origem com um fade em forma de retangular.  <br/> |
|13   <br/> |Gradiente do caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **FillGradientDir** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FillGradientDir  <br/> |
   
Para fazer referência à célula **FillGradientDir** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice de célula:  <br/> |**visFillGradientDir** <br/> |
   

