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
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358979"
---
# <a name="linerouteext-cell-page-layout-section"></a>Célula LineRouteExt (Seção Page Layout)

Determina a aparência padrão de todos os conectores em uma página de desenho.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Padrão (reto)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Estreita  <br/> |**visLORouteExtStraight** <br/> |
| duas  <br/> | Curvo  <br/> |**visLORouteExtNURBS** <br/> |
   
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
   

