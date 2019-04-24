---
title: Célula ShdwObliqueAngle (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Contém um número que especifica o ângulo de direção oblíqua na aplicação do tipo de sombra padrão da página.
ms.openlocfilehash: 2eca29bbc735c7101ca82a2f26db30b2e344b8e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349060"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>Célula ShdwObliqueAngle (Seção Page Properties)

Contém um número que especifica o ângulo de direção oblíqua na aplicação do tipo de sombra padrão da página.
  
## <a name="remarks"></a>Comentários

Um valor zero (0) nesta célula indica que a direção do ângulo é reta, para cima, e ele é medido no sentido horário.
  
 O ângulo descrito nesta célula é usado sempre que a célula ShapeShdwType (o tipo de sombra para uma forma na página) é definida como padrão da página (**visFSTPageDefault** ), e o tipo de sombra é oblíquo. O tipo de sombra padrão da página é definido na célula ShdwType. 
  
Para configurar este comportamento para uma forma individual, use a célula ShapeShdwObliqueAngle na seção Fill Format.
  
Para fazer referência à célula ShdwObliqueAngle pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwObliqueAngle  <br/> |
   
Para fazer referência à célula ShdwObliqueAngle pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageShdwObliqueAngle** <br/> |
   

