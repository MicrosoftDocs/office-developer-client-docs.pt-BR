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
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415800"
---
# <a name="denoise-cell-image-properties-section"></a>Célula Clareza (Seção Imagem Propriedades)

Remove os ruídos (pixels com níveis de cor distribuídos aleatoriamente) de uma imagem de bitmap. O valor padrão é 0%.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Denoise pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Clareza  <br/> |
   
Para fazer referência à célula Denoise pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowImage** <br/> |
| Índice de célula:  <br/> |**visImageDenoise** <br/> |
   

