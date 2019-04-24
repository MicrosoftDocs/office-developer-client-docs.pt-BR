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
description: Representa uma sequência de caracteres que passa as informações que serão utilizadas para resolver um URL, como as coordenadas de um mapa de imagens. Por exemplo, na célula ExtraInfo, x = 41&amp;y = 7specifies as coordenadas de um mapa de imagem.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357817"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>Célula ExtraInfo (Seção Hyperlinks)

Representa uma sequência de caracteres que passa as informações que serão utilizadas para resolver um URL, como as coordenadas de um mapa de imagens. Por exemplo, na célula ExtraInfo, "x = 41&amp;y = 7" especifica as coordenadas de um mapa de imagem.
  
## <a name="remarks"></a>Comentários

As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.
  
Para fazer referência à célula ExtraInfo pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hiperlink.  *nome* . ExtraInfo onde hiperlink.  *Name* é o nome da linha  <br/> |
   
Para fazer referência à célula ExtraInfo pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHiperlink** <br/> |
| Índice de linha:  <br/> |**visRow1stHyperlink** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visHLinkExtraInfo** <br/> |
   

