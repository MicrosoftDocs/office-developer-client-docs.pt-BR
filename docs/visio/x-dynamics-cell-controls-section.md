---
title: Célula X Dynamics (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Representa o x-coordenadas para o ponto de ancoragem de uma alça de controle em coordenadas locais.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773326"
---
# <a name="x-dynamics-cell-controls-section"></a>Célula X Dynamics (Seção Controls)

Representa o *x* -coordenadas para o ponto de ancoragem de uma alça de controle em coordenadas locais. 
  
## <a name="remarks"></a>Comentários

O ponto de ancoragem é utilizado para esticar durante a dinâmica.
  
Para fazer referência à célula X Dynamics pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Controles.  *nome* . Controles de XDynwhere.  *nome* é o nome da linha controles.  <br/> |
   
Para fazer referência à célula X Dynamics pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice da linha:  <br/> |**visRowControl** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCtlXDyn** <br/> |
   

