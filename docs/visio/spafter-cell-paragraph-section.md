---
title: Célula SpAfter (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Determina a quantidade de espaço inserido depois de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o último parágrafo em um bloco de texto, da célula BottomMargin.
ms.openlocfilehash: 2b8fe7e2b0df09561d0db4367f917c8f4b71335d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335221"
---
# <a name="spafter-cell-paragraph-section"></a>Célula SpAfter (Seção Paragraph)

Determina a quantidade de espaço inserido depois de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o último parágrafo em um bloco de texto, da célula BottomMargin.
  
## <a name="remarks"></a>Comentários

Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a definição de Espaço após será a mesma.
  
Para fazer referência à célula SpAfter pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para. antes de [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula SpAfter pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice da linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSpaceAfter** <br/> |
   

