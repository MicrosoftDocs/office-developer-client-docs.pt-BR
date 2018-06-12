---
title: Célula NoSnap (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Determina se outras formas serão ajustadas a um caminho.
ms.openlocfilehash: 111f3773cb1df9033ed5a7b0b146d40ce6b26df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772425"
---
# <a name="nosnap-cell-geometry-section"></a>Célula NoSnap (Seção Geometry)

Determina se outras formas serão ajustadas a um caminho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Não permitir que outras formas sejam ajustadas a este caminho.  <br/> |
| FALSO  <br/> | Permitir que outras formas sejam ajustadas a este caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula NoSnap pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometria *i* . NoSnap onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula NoSnap pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowComponent** <br/> |
| Índice da célula:  <br/> |**visCompNoSnap** <br/> |
   

