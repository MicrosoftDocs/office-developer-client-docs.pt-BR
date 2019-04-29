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
description: Determina se outras formas se ajustarão a um caminho.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408541"
---
# <a name="nosnap-cell-geometry-section"></a>Célula NoSnap (Seção Geometry)

Determina se outras formas se ajustarão a um caminho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Não permitir que outras formas sejam ajustadas a este caminho.  <br/> |
| FALSE  <br/> | Permitir que outras formas sejam ajustadas a este caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula NoSnap pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry *i* . NoSnap onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula NoSnap pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowComponent** <br/> |
| Índice da célula:  <br/> |**visCompNoSnap** <br/> |
   

