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
ms.openlocfilehash: 93db93e58124b5f176fb57f843580eff6a3d4d3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773065"
---
# <a name="spafter-cell-paragraph-section"></a>Célula SpAfter (Seção Paragraph)

Determina a quantidade de espaço inserido depois de cada parágrafo no bloco de texto da forma, além de qualquer espaço da célula SpLine e, caso seja o último parágrafo em um bloco de texto, da célula BottomMargin.
  
## <a name="remarks"></a>Comentários

Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a definição de Espaço após será a mesma.
  
Para obter uma referência à célula SpAfter pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para.SpAfter [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula SpAfter pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice da linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSpaceAfter** <br/> |
   

