---
title: Célula FillGradientDir (seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina a direção do gradiente de preenchimento. Um gradiente pode ser linear, radial, retangular ou seguir um caminho.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322460"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>Célula FillGradientDir (seção Gradient Properties)

Determina a direção do gradiente de preenchimento. Um gradiente pode ser linear, radial, retangular ou seguir um caminho. 
  
> [!NOTE]
> Um gradiente linear é o único gradiente que assume um valor de ângulo adicional (conforme determinado pela célula **FillGradientDir** ). Todas as outras direções de gradiente têm enumerações predefinidas. 
  
****

|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |Gradiente linear. A célula **FillGradientAngle** determina a direção do gradiente.  <br/> |
|1-7  <br/> |Gradientes radiais. O gradiente se estende para cima em um círculo a partir de um ponto central.  <br/> |
|8-12  <br/> |Gradientes retangulares. O gradiente estende-se como uma linha direcional de uma origem com um esmaecimento de forma retangular.  <br/> |
|Treze  <br/> |Gradiente de caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **FillGradientDir** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FillGradientDir  <br/> |
   
Para obter uma referência para a célula **FillGradientDir** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |**visFillGradientDir** <br/> |
   

