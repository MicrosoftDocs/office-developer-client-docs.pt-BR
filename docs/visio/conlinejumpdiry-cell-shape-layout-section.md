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
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404768"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>Célula ConLineJumpDirY (Seção Shape Layout)

Determina a direção dos saltos de linha que ocorrem em um conector dinâmico vertical para uma forma.
  
|**Valor**|**Direção do salto de linha**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Padrão da página  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Esquerdo  <br/> |**visLOJumpDirYLeft** <br/> |
| duas  <br/> | À direita  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Comentários

Para definir a direção vertical padrão para *todos os* saltos de conectores em uma página, use a célula PageLineJumpDirY na seção Page Layout. 
  
Para fazer referência à célula ConLineJumpDirY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ConLineJumpDirY  <br/> |
   
Para fazer referência à célula ConLineJumpDirY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
| Índice de célula:  <br/> |**visSLOJumpDirY** <br/> |
   

