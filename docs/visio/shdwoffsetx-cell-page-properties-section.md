---
title: Célula ShdwOffsetX (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada horizontalmente da forma.
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772948"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a>Célula ShdwOffsetX (Seção Page Properties)

Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada horizontalmente da forma.
  
## <a name="remarks"></a>Comentários

Esse valor é definido na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ). Esse valor é independente da escala do desenho. Se o desenho estiver em escala, o deslocamento de sombra permanece o mesmo. 
  
Para obter uma referência para a célula ShdwOffsetX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwOffsetX  <br/> |
   
Para obter uma referência para a célula ShdwOffsetX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageShdwOffsetX** <br/> |
   

