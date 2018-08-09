---
title: Célula LineGradientDir (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Determina a direção do gradiente linha. Um gradiente pode ser linear, radial, retangular ou seguem um caminho.
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772204"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>Célula LineGradientDir (Seção Gradient Properties)

Determina a direção do gradiente linha. Um gradiente pode ser linear, radial, retangular ou seguem um caminho. 
  
> [!NOTE]
> Um gradiente linear é o gradiente único que tem um valor de ângulo adicionais (conforme determinado pela célula **LineGradientDir** ). Todas as outras direções gradientes têm predefinidas enumerações. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Gradiente linear. A célula **LineGradientAngle** determina a direção do gradiente.  <br/> |
|1 a 7  <br/> |Gradientes radiais. Gradiente estende para fora de um círculo de um ponto central.  <br/> |
|8-12  <br/> |Gradientes retangulares. Estende o gradiente como uma linha direcional de uma origem com um esmaecer retangular.  <br/> |
|13  <br/> |Gradiente de caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **LineGradientDir** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LineGradientDir  <br/> |
   
Para obter uma referência à célula **LineGradientDir** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |**visLineGradientDir** <br/> |
   

