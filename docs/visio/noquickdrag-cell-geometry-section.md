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
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772424"
---
# <a name="noquickdrag-cell-geometry-section"></a>Célula NoQuickDrag (Seção Geometry)

Determina se uma forma pode ser selecionada ou arrastada quando o usuário clica na área preenchida definida pela seção Geometry.
  
## <a name="remarks"></a>Comentários

Para obter uma referência à célula NoQuickDrag pelo nome a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Geometria *i* . NoQuickDrag, onde * i * - < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula NoQuickDrag pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* , onde *i* = 0, 1, 2...  <br/> |
|Índice da linha:  <br/> |**visRowComponent** <br/> |
|Índice da célula:  <br/> |**visCompNoQuickDrag** <br/> |
   

