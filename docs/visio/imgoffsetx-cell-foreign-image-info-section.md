---
title: Célula ImgOffsetX (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251308
localization_priority: Normal
ms.assetid: c079fb10-4db7-4657-75d2-2fb953c86670
description: Determina a distância de deslocamento horizontal do objeto em relação à origem de sua borda. O padrão é 0. Deslocar o objeto com a ferramenta Cortar irá alterar esse valor.
ms.openlocfilehash: dda385b2157e48baec2b21c6da741b31d05c3291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772065"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a>Célula Cell (Foreign Image Info Section) (Seção Foreign Image Info)

Determina a distância de deslocamento horizontal do objeto em relação à origem de sua borda. O padrão é 0. Deslocar o objeto com a ferramenta **Cortar** irá alterar esse valor. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula ImgOffsetX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ImgOffsetX  <br/> |
   
Para fazer referência à célula ImgOffsetX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowForeign** <br/> |
| Índice da célula:  <br/> |**visFrgnImgOffsetX** <br/> |
   

