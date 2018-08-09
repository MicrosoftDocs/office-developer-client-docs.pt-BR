---
title: Célula PageLineJumpDirY (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Determina a direção dos saltos de linha em conectores dinâmicos verticais na página de desenho para a qual uma direção de salto local não foi aplicada.
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772464"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>Célula LineJumpDirY (Seção Page Layout)

Determina a direção dos saltos de linha em conectores dinâmicos verticais na página de desenho para a qual uma direção de salto local não foi aplicada.
  
|**Valor**|**Direção do salto de linha**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Padrão; acima ou a definição da página para formas  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Esquerda  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Direita  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula PageLineJumpDirY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageLineJumpDirY  <br/> |
   
Para fazer referência à célula PageLineJumpDirY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLOJumpDirY** <br/> |
   

