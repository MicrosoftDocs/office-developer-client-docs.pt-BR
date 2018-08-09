---
title: Célula Blur (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm115
localization_priority: Normal
ms.assetid: 8b077cdb-6036-4f77-dc20-a476bb75b0f7
description: Esfuma ou suaviza uma imagem de bitmap. O valor padrão é 0%.
ms.openlocfilehash: 14a50f2015b2b24d7e41f5d11018a749d089fc37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771408"
---
# <a name="blur-cell-image-properties-section"></a>Célula Blur (Seção Image Properties)

Esfuma ou suaviza uma imagem de bitmap. O valor padrão é 0%.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Blur pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Blur  <br/> |
   
Para fazer referência à célula Blur pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowImage** <br/> |
| Índice da célula:  <br/> |**visImageBlur** <br/> |
   

