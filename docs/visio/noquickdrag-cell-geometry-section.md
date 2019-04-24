---
title: Célula NoQuickDrag (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Determina se uma forma pode ser selecionada ou arrastada quando o usuário clica na área preenchida definida pela seção Geometry.
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341059"
---
# <a name="noquickdrag-cell-geometry-section"></a>Célula NoQuickDrag (Seção Geometry)

Determina se uma forma pode ser selecionada ou arrastada quando o usuário clica na área preenchida definida pela seção Geometry.
  
## <a name="remarks"></a>Comentários

Para obter uma referência à célula NoQuickDrag pelo nome a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Geometry *i* . NoQuickDrag, onde * i *-<1>, 2, 3...  <br/> |
   
Para obter uma referência à célula NoQuickDrag pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* , onde *i* = 0, 1, 2...  <br/> |
|Índice da linha:  <br/> |**visRowComponent** <br/> |
|Índice da célula:  <br/> |**visCompNoQuickDrag** <br/> |
   

