---
title: Célula ConLineRouteExt (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Determina a aparência de um conector.
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434610"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>Célula ConLineRouteExt (Seção Shape Layout)

Determina a aparência de um conector.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Padrão; utiliza a configuração de página  <br/> |**visLORouteExtDefault** <br/> |
| 1   <br/> | Reto  <br/> |**visLORouteExtStraight** <br/> |
| 2   <br/> | Curvo  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula ConLineRouteExt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ConLineRouteExt  <br/> |
   
Para fazer referência à célula ConLineRouteExt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
| Índice de célula:  <br/> |**visSLOLineRouteExt** <br/> |
   

