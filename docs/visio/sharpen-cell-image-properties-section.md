---
title: Célula Sharpen (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: Ajusta a nitidez de uma imagem de bitmap. O valor padrão é 0%. Ajustar a nitidez focaliza uma imagem aumentando o contraste dos pixels adjacentes.
ms.openlocfilehash: fbc66f8c88cde67ad1f259f8392f6d3bd0457be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772937"
---
# <a name="sharpen-cell-image-properties-section"></a>Célula Sharpen (Seção Image Properties)

Ajusta a nitidez de uma imagem de bitmap. O valor padrão é 0%. Ajustar a nitidez focaliza uma imagem aumentando o contraste dos pixels adjacentes.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Sharpen pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Sharpen  <br/> |
   
Para fazer referência à célula Sharpen pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowImage** <br/> |
| Índice da célula:  <br/> |**visImageSharpen** <br/> |
   

