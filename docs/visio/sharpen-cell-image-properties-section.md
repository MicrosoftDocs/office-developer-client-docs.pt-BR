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
ms.openlocfilehash: e519cf6e5a168b64b4bc8aa083843163a47525ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349088"
---
# <a name="sharpen-cell-image-properties-section"></a>Célula Sharpen (Seção Image Properties)

Ajusta a nitidez de uma imagem de bitmap. O valor padrão é 0%. Ajustar a nitidez focaliza uma imagem aumentando o contraste dos pixels adjacentes.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Sharpen pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Nitidez  <br/> |
   
Para fazer referência à célula Sharpen pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowImage** <br/> |
| Índice da célula:  <br/> |**visImageSharpen** <br/> |
   

