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
ms.openlocfilehash: f0a27090ea1ec96bf11726ae641ff918dd581e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404922"
---
# <a name="contrast-cell-image-properties-section"></a>Célula Contrast (Seção Image Properties)

Ajusta o contraste de uma imagem de bitmap. Diminua o contraste de uma imagem inserindo um valor entre 0% e 49% ou aumente o contraste inserindo um valor entre 51% e 100%. O valor padrão é 50%.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Contrast pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Contraste  <br/> |
   
Para fazer referência à célula Contrast pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowImage** <br/> |
| Índice de célula:  <br/> |**visImageContrast** <br/> |
   

