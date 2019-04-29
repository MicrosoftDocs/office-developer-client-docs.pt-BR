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
ms.openlocfilehash: 599810d126c853e37552045d0ef83cb580606ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427903"
---
# <a name="blur-cell-image-properties-section"></a>Célula Blur (Seção Image Properties)

Esfuma ou suaviza uma imagem de bitmap. O valor padrão é 0%.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Blur pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Desfoque  <br/> |
   
Para fazer referência à célula Blur pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowImage** <br/> |
| Índice de célula:  <br/> |**visImageBlur** <br/> |
   

