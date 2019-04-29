---
title: Célula NoLine (Seção Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Determina se uma linha será desenhada em torno do limite do caminho.
ms.openlocfilehash: ad3744ae8deb4ffb4dd2282e50590439c4b218a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433749"
---
# <a name="noline-cell-geometry-section"></a>Célula NoLine (Seção Geometry)

Determina se uma linha será desenhada em torno do limite do caminho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Uma linha não é desenhada em torno do limite do caminho que é o limite de uma região preenchida.  <br/> |
| FALSE  <br/> | Uma linha é desenhada em torno do limite de um caminho.  <br/> |
   
## <a name="remarks"></a>Comentários

Ao alterar a cor de uma linha para branca, a linha continuará a existir embora não seja possível visualizá-la em um plano de fundo branco. Se o valor da célula for definido para VERDADEIRO, nenhuma linha será desenhada.
  
Para fazer referência à célula NoLine pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Geometry *i* . NoLine onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula NoLine pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionFirstComponent** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da linha:  <br/> |**visRowComponent** <br/> |
| Índice da célula:  <br/> |**visCompNoLine** <br/> |
   

