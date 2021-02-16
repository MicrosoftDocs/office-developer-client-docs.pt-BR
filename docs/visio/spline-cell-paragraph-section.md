---
title: Célula SpLine (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Determina a distância entre uma linha do texto e a próxima, expressa em porcentagem, sendo 100% a altura da linha de um texto.
ms.openlocfilehash: 82b2604a62608c0cc4333892d678b1eb886a9c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434911"
---
# <a name="spline-cell-paragraph-section"></a>Célula SpLine (Seção Paragraph)

Determina a distância entre uma linha do texto e a próxima, expressa em porcentagem, sendo 100% a altura da linha de um texto.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| \>0  <br/> | Espaçamento absoluto, independentemente do tamanho da fonte  <br/> |
| =0  <br/> | Definir sólido (espaçamento = 100% do tamanho da fonte)  <br/> |
| \<0  <br/> | Uma porcentagem do tamanho da fonte (por exemplo, -120% produz 120% de espaçamento)  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula SpLine pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Para. SpLine [  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula SpLine pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionParagraph** <br/> |
| Índice de linha:  <br/> |**visRowParagraph**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSpaceLine** <br/> |
   

