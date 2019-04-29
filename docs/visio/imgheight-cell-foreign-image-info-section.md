---
title: Célula ImgWidth (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Determina a altura da imagem do objeto dentro de sua borda. A fórmula padrão é:'
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411194"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>Célula ImgWidth (Seção Foreign Image Info)

Determina a altura da imagem do objeto dentro de sua borda. A fórmula padrão é:
  
= Altura \* 1
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula ImgHeight pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ImgHeight  <br/> |
   
Para fazer referência à célula ImgHeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowForeign** <br/> |
| Índice da célula:  <br/> |**visFrgnImgHeight** <br/> |
   

