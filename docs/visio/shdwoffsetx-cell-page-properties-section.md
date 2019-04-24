---
title: Célula ShdwOffsetX (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada horizontalmente da forma.
ms.openlocfilehash: fbc7d37fc8ba45f3219af6a4350301102954f23d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338749"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a>Célula ShdwOffsetX (Seção Page Properties)

Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada horizontalmente da forma.
  
## <a name="remarks"></a>Comentários

Esse valor é definido na caixa de diálogo **Configurar página** (na guia **Design**, clique na seta **Configurar Página**). Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o deslocamento da sombra será o mesmo. 
  
Para obter uma referência para a célula ShdwOffsetX pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwOffsetX  <br/> |
   
Para obter uma referência para a célula ShdwOffsetX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageShdwOffsetX** <br/> |
   

