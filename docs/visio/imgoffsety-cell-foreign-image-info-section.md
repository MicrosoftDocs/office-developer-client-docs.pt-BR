---
title: Célula ImgOffsetY (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm455
localization_priority: Normal
ms.assetid: 3b2991aa-4722-fe3b-39c5-02d38c4c7efc
description: Determina a distância de deslocamento vertical do objeto em relação à origem de sua borda. O padrão é 0. Deslocar o objeto com a ferramenta Cortar irá alterar esse valor.
ms.openlocfilehash: 2930aa092a2b776ceb0c9c4677f7e5da7f5dcdda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772058"
---
# <a name="imgoffsety-cell-foreign-image-info-section"></a>Célula ImgOffsetY (Seção Foreign Image Info)

Determina a distância de deslocamento vertical do objeto em relação à origem de sua borda. O padrão é 0. Deslocar o objeto com a ferramenta **Cortar** irá alterar esse valor. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula ImgOffsetY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ImgOffsetY  <br/> |
   
Para fazer referência à célula ImgOffsetY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowForeign** <br/> |
| Índice da célula:  <br/> |**visFrgnImgOffsetY** <br/> |
   

