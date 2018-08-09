---
title: Célula LineJumpStyle (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251646
localization_priority: Normal
ms.assetid: 89f16674-ee1f-f5f9-9830-7bcc52e3a068
description: Determina o estilo de salto de linha de todos os conectores na página de desenho sem um estilo de salto de linha local.
ms.openlocfilehash: 96941f675b67b38a8575bd712db5ad0eb76cd50f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772203"
---
# <a name="linejumpstyle-cell-page-layout-section"></a>Célula LineJumpStyle (Seção Page Layout)

Determina o estilo de salto de linha de todos os conectores na página de desenho sem um estilo de salto de linha local.
  
|**Valor**|**Estilo de salto de linha**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Arco  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arco  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Intervalo  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Quadrado  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |2 lados  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 lados  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 lados  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 lados  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 lados  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 lados  <br/> |**visLOJumpStyle6Point** <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).
  
Para obter uma referência à célula LineJumpStyle pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineJumpStyle  <br/> |
   
Para obter uma referência à célula LineJumpStyle pelo índice, em outro programa que use a propriedade **CellsSRC**, utilize: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLOJumpStyle** <br/> |
   

