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
description: Representa a coordenada x do ponto de ancoragem de uma alça de controle em coordenadas locais.
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432125"
---
# <a name="x-dynamics-cell-controls-section"></a>Célula X Dynamics (Seção Controls)

Representa a  *coordenada x*  do ponto de ancoragem de uma alça de controle em coordenadas locais. 
  
## <a name="remarks"></a>Comentários

O ponto de ancoragem é utilizado para esticar durante a dinâmica.
  
Para fazer referência à célula X Dynamics pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Controles.  *nome*  . Controles XDynwhere.  *é*  o nome da linha de controles.  <br/> |
   
Para fazer referência à célula X Dynamics pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice de linha:  <br/> |**visRowControl**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCtlXDyn** <br/> |
   

