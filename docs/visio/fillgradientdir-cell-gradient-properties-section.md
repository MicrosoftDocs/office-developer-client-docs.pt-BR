---
title: Célula FillGradientDir (seção Propriedades de gradiente)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina a direção do gradiente do preenchimento. Um gradiente pode ser linear, radial, retangular ou seguem um caminho.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771868"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>Célula FillGradientDir (seção Propriedades de gradiente)

Determina a direção do gradiente do preenchimento. Um gradiente pode ser linear, radial, retangular ou seguem um caminho. 
  
> [!NOTE]
> Um gradiente linear é o gradiente único que tem um valor de ângulo adicionais (conforme determinado pela célula **FillGradientDir** ). Todas as outras direções gradientes têm predefinidas enumerações. 
  
****

|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Gradiente linear. A célula **FillGradientAngle** determina a direção do gradiente.  <br/> |
|1 a 7  <br/> |Gradientes radiais. Gradiente estende para fora de um círculo de um ponto central.  <br/> |
|8-12  <br/> |Gradientes retangulares. Estende o gradiente como uma linha direcional de uma origem com um esmaecer retangular.  <br/> |
|13  <br/> |Gradiente de caminho.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Para fazer referência à célula **FillGradientDir** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FillGradientDir  <br/> |
   
Para obter uma referência à célula **FillGradientDir** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |**visFillGradientDir** <br/> |
   

