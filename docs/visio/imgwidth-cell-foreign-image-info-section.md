---
title: Célula ImgWidth (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Determina a largura da imagem do objeto dentro de sua borda. A fórmula padrão é:'
ms.openlocfilehash: 9da5e06a7fbf6ae77a49fb0410aefb406e2afecb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344720"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>Célula ImgWidth (Seção Foreign Image Info)

Determina a largura da imagem do objeto dentro de sua borda. A fórmula padrão é:
  
= Largura \* 1
  
Cortar o objeto altera o fator pelo qual a largura é multiplicada.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula ImgWidth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ImgWidth  <br/> |
   
Para fazer referência à célula ImgWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowForeign** <br/> |
| Índice da célula:  <br/> |**visFrgnImgWidth** <br/> |
   

