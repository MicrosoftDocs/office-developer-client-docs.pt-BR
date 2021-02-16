---
title: Célula ConLineJumpDirX (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Determina a direção dos saltos de linha que ocorrem em um conector dinâmico horizontal para uma forma.
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415037"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>Célula ConLineJumpDirX (Seção Shape Layout)

Determina a direção dos saltos de linha que ocorrem em um conector dinâmico horizontal para uma forma.
  
|**Valor**|**Direção do salto de linha**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Padrão da página  <br/> |**visLOJumpDirXDefault** <br/> |
| 1   <br/> | Para cima  <br/> |**visLOJumpDirXUp** <br/> |
| 2   <br/> | Para baixo  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Comentários

Para definir a direção  horizontal padrão para todos os saltos de conector em uma página, use a célula PageLineJumpDirX na seção Page Layout. 
  
Para fazer referência à célula ConLineJumpDirX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ConLineJumpDirX  <br/> |
   
Para fazer referência à célula ConLineJumpDirX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
| Índice de célula:  <br/> |**visSLOJumpDirX** <br/> |
   

