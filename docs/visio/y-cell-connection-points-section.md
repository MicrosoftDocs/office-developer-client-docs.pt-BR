---
title: Célula Y (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Representa o y-coordenadas de um ponto de conexão em coordenadas locais.
ms.openlocfilehash: 270ae98789e29ca170f260aa70e951d4b2af2962
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773311"
---
# <a name="y-cell-connection-points-section"></a>Célula Y (Seção Connection Points)

Representa o *y* -coordenadas de um ponto de conexão em coordenadas locais. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Y pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Connections.Y *i* onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula Y pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
| Índice da linha:  <br/> |**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visY** <br/> |
   

