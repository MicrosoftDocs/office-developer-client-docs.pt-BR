---
title: Célula Angle (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Representa o ângulo de rotação atual da forma em relação ao pai. A fórmula padrão para determinar o ângulo de rotação de uma forma 1D é: =ATAN2(EndY-BeginY,EndX-BeginX).'
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341465"
---
# <a name="angle-cell-shape-transform-section"></a>Célula Angle (Seção Shape Transform)

Representa o ângulo de rotação atual da forma em relação ao pai. A fórmula padrão para determinar o ângulo de rotação de uma forma 1D é: =ATAN2(EndY-BeginY,EndX-BeginX).
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Angle pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Ângulo  <br/> |
   
Para fazer referência à célula Angle pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowXFormOut** <br/> |
| Índice da célula:  <br/> |**visXFormAngle** <br/> |
   

