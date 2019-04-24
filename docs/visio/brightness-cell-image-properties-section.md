---
title: Célula Brightness (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
localization_priority: Normal
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: Ajusta o brilho de uma imagem de bitmap. Diminua o brilho de uma imagem inserindo um valor entre 0% e 49% ou aumente o brilho inserindo um valor entre 51% e 100%. O valor padrão é 50%.
ms.openlocfilehash: ae1390d2db3adad86a8afcbeaff88172a841d030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338021"
---
# <a name="brightness-cell-image-properties-section"></a>Célula Brightness (Seção Image Properties)

Ajusta o brilho de uma imagem de bitmap. Diminua o brilho de uma imagem inserindo um valor entre 0% e 49% ou aumente o brilho inserindo um valor entre 51% e 100%. O valor padrão é 50%.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Brightness pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Brilho  <br/> |
   
Para fazer referência à célula Brightness pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowImage** <br/> |
| Índice da célula:  <br/> |**visImageBrightness** <br/> |
   

