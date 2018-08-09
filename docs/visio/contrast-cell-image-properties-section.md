---
title: Célula Contrast (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm200
localization_priority: Normal
ms.assetid: f0e4c644-c646-9649-c697-82feb02f5e29
description: Ajusta o contraste de uma imagem de bitmap. Diminua o contraste de uma imagem inserindo um valor entre 0% e 49% ou aumente o contraste inserindo um valor entre 51% e 100%. O valor padrão é 50%.
ms.openlocfilehash: 74a82fd9be49fcb9126c2b52bfcf25e0deb0e782
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771604"
---
# <a name="contrast-cell-image-properties-section"></a>Célula Contrast (Seção Image Properties)

Ajusta o contraste de uma imagem de bitmap. Diminua o contraste de uma imagem inserindo um valor entre 0% e 49% ou aumente o contraste inserindo um valor entre 51% e 100%. O valor padrão é 50%.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Contrast pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Contrast  <br/> |
   
Para fazer referência à célula Contrast pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowImage** <br/> |
| Índice da célula:  <br/> |**visImageContrast** <br/> |
   

