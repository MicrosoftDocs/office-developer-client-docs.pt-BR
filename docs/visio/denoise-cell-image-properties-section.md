---
title: Célula Denoise (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Remove os ruídos (pixels com níveis de cor distribuídos aleatoriamente) de uma imagem de bitmap. O valor padrão é 0%.
ms.openlocfilehash: f08d09126a24935c0dd4dcda5e88fdd559c8d176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771720"
---
# <a name="denoise-cell-image-properties-section"></a>Célula Denoise (Seção Image Properties)

Remove os ruídos (pixels com níveis de cor distribuídos aleatoriamente) de uma imagem de bitmap. O valor padrão é 0%.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Denoise pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Denoise  <br/> |
   
Para fazer referência à célula Denoise pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowImage** <br/> |
| Índice da célula:  <br/> |**visImageDenoise** <br/> |
   

