---
title: Célula ConLineJumpDirY (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Determina a direção dos saltos de linha que ocorrem em um conector dinâmico vertical para uma forma.
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771561"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>Célula ConLineJumpDirY (Seção Shape Layout)

Determina a direção dos saltos de linha que ocorrem em um conector dinâmico vertical para uma forma.
  
|**Valor**|**Direção do salto de linha**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Padrão da página  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Esquerdo  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | À direita  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Coment�rios

Para definir o padrão direção vertical para *todos os* conector salta em uma página, utilize a célula PageLineJumpDirY na seção Page Layout. 
  
Para obter uma referência à célula ConLineJumpDirY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ConLineJumpDirY  <br/> |
   
Para obter uma referência à célula ConLineJumpDirY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
| Índice da célula:  <br/> |**visSLOJumpDirY** <br/> |
   

