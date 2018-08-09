---
title: Célula ExtraInfo (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Representa uma cadeia de caracteres que passa informações a serem usadas na resolução de uma URL, como as coordenadas de um mapa de imagem. Por exemplo, na célula ExtraInfo, x = 41&amp;y = 7specifies as coordenadas de um mapa de imagem.
ms.openlocfilehash: aa035d5ec863cd8045063af970efa26b53683793
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771847"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>Célula ExtraInfo (Seção Hyperlinks)

Representa uma cadeia de caracteres que passa informações a serem usadas na resolução de uma URL, como as coordenadas de um mapa de imagem. Por exemplo, na célula ExtraInfo, "x = 41&amp;y = 7" Especifica as coordenadas de um mapa de imagem.
  
## <a name="remarks"></a>Comentários

As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.
  
Para fazer referência à célula ExtraInfo pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hiperlink.  *nome* . ExtraInfo onde Hyperlink.  *Name* é o nome da linha  <br/> |
   
Para fazer referência à célula ExtraInfo pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHyperlink** <br/> |
| Índice da linha:  <br/> |**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visHLinkExtraInfo** <br/> |
   

