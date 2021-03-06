---
title: Célula Y Dynamics (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Representa a coordenada y do ponto de ancoragem de uma alça de controle em coordenadas locais. O ponto de ancoragem é utilizado para esticar durante a dinâmica.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404824"
---
# <a name="y-dynamics-cell-controls-section"></a>Célula Y Dynamics (Seção Controls)

Representa a  *coordenada y*  do ponto de ancoragem de uma alça de controle em coordenadas locais. O ponto de ancoragem é utilizado para esticar durante a dinâmica. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Y Dynamics pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Controles.  *nome*  . Controles YDynwhere.  *é*  o nome da linha de controles.  <br/> |
   
Para fazer referência à célula Y Dynamics pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice de linha:  <br/> |**visRowControl**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCtlYDyn** <br/> |
   

