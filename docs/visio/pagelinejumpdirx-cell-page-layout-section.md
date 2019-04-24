---
title: Célula PageLineJumpDirX (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Determina a direção dos saltos de linha em conectores dinâmicos horizontais na página de desenho para a qual uma direção de salto local não foi aplicada.
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283734"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>Célula PageLineJumpDirX (Seção Page Layout)

Determina a direção dos saltos de linha em conectores dinâmicos horizontais na página de desenho para a qual uma direção de salto local não foi aplicada.
  
|**Valor**|**Direção do salto de linha**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Padrão; à esquerda ou a definição da página para formas  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Para cima  <br/> |**visLOJumpDirXUp** <br/> |
| duas  <br/> | Para baixo  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula PageLineJumpDirX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageLineJumpDirX  <br/> |
   
Para fazer referência à célula PageLineJumpDirX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLOJumpDirX** <br/> |
   

