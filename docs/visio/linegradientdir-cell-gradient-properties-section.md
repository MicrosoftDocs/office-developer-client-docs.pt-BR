---
title: Célula LineGradientDir (seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Determina a direção do gradiente de linha. Um gradiente pode ser linear, radial, retangular ou seguir um caminho.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417984"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>Célula LineGradientDir (seção Gradient Properties)

Determina a direção do gradiente de linha. Um gradiente pode ser linear, radial, retangular ou seguir um caminho. 
  
> [!NOTE]
> Um gradiente linear é o único gradiente que assume um valor de ângulo adicional (conforme determinado pela célula **LineGradientDir** ). Todas as outras direções de gradiente têm enumerações predefinidas. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |Gradiente linear. A célula **LineGradientAngle** determina a direção do gradiente.  <br/> |
|1-7  <br/> |Gradientes radiais. O gradiente se estende para cima em um círculo a partir de um ponto central.  <br/> |
|8-12  <br/> |Gradientes retangulares. O gradiente estende-se como uma linha direcional de uma origem com um esmaecimento de forma retangular.  <br/> |
|13   <br/> |Gradiente de caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **LineGradientDir** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LineGradientDir  <br/> |
   
Para obter uma referência para a célula **LineGradientDir** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |**visLineGradientDir** <br/> |
   

