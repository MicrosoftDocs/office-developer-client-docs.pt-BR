---
title: Célula NoShow (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Indica se um caminho será exibido na página de desenho.
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410347"
---
# <a name="noshow-cell-geometry-section"></a>Célula NoShow (Seção Geometry)

Indica se um caminho será exibido na página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | O traço e o preenchimento do caminho representados pela seção estão ocultos.  <br/> |
| FALSE  <br/> | O traço e o preenchimento do caminho são exibidos.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula NoShow pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry *i* . NoShow onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula NoShow pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowComponent** <br/> |
| Índice da célula:  <br/> |**visCompNoShow** <br/> |
   

