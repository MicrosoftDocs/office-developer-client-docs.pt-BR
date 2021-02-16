---
title: Célula ShapeSplittable (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Indica se a forma 1D pode ser dividida.
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427070"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>Célula ShapeSplittable (Seção Shape Layout)

Indica se a forma 1D pode ser dividida. 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Não permitir a divisão desta forma.  <br/> |**visSLOSplittableNone** <br/> |
| 1   <br/> | Permitir a divisão desta forma.  <br/> |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>Comentários

O comportamento padrão de conectores e outras formas 1D varia por tipo de desenho. 
  
A divisão automática de formas é habilitada e desabilitada em três níveis diferentes: aplicativo, página e forma. Por padrão, a divisão é habilitada nos níveis do aplicativo e da página. 
  
Para habilitar ou desabilitar a  divisão no nível do aplicativo, use a configuração  de divisão do conector Habilitar na guia Avançado da caixa de diálogo Opções do **Visio** (clique na guia Arquivo, clique em Opções e em  **Avançado).** 
  
Para habilitar ou desabilitar a divisão em uma página, consulte a célula [PageShapeSplit](pageshapesplit-cell-page-layout-section.md). 
  
Para fazer com que uma forma possa dividir formas 1D divisíveis, consulte a célula [ShapeSplit](shapesplit-cell-shape-layout-section.md). 
  
Para fazer referência à célula ShapeSplittable pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShapeSplittable  <br/> |
   
Para fazer referência à célula ShapeSplittable pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
| Índice de célula:  <br/> |**visSLOSplittable** <br/> |
   

