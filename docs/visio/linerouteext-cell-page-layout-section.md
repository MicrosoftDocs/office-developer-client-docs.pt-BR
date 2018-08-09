---
title: Célula LineRouteExt (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Determina a aparência padrão de todos os conectores em uma página de desenho.
ms.openlocfilehash: 21da283f2d9ab43837b8fe4127840e89ea9d9949
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772216"
---
# <a name="linerouteext-cell-page-layout-section"></a>Célula LineRouteExt (Seção Page Layout)

Determina a aparência padrão de todos os conectores em uma página de desenho.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Padrão (reto)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Reto  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Curvado  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LineRouteExt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LineRouteExt  <br/> |
   
Para fazer referência à célula LineRouteExt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLOLineRouteExt** <br/> |
   

