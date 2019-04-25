---
title: Célula ConLineJumpStyle (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: Determina o estilo de salto da linha para os saltos de linha em um conector dinâmico.
ms.openlocfilehash: ae8af4e326a6c895b3617a4869f98eaf0db68db1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360057"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>Célula ConLineJumpStyle (Seção Shape Layout)

Determina o estilo de salto da linha para os saltos de linha em um conector dinâmico.
  
|**Valor**|**Estilo de salto de linha**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Padrão da página  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Lacuna  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Quadrado  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |Triângulo  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 lados  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 lados  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 lados  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 lados  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 lados  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice de célula:  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o valor desta célula selecionando um conector dinâmico, clicando em **Comportamento**, no grupo **Design da Forma**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **Conector**. 
  
Para obter uma referência à célula ConLineJumpStyle por nome de outra fórmula ou de um programa que utiliza a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ConLineJumpStyle  <br/> |
   
Para obter uma referência à célula ConLineJumpStyle por índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  

