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
ms.openlocfilehash: ad4d9cf1aa3e541f512bc09ffc38cf03204b3c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772449"
---
# <a name="noshow-cell-geometry-section"></a>Célula NoShow (Seção Geometry)

Indica se um caminho será exibido na página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | O traço e o preenchimento do caminho representados pela seção estão ocultos.  <br/> |
| FALSO  <br/> | O traço e o preenchimento do caminho são exibidos.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula NoShow pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometria *i* . NoShow onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula NoShow pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowComponent** <br/> |
| Índice da célula:  <br/> |**visCompNoShow** <br/> |
   

