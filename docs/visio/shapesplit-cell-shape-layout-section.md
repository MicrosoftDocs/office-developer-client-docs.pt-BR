---
title: Célula ShapeSplit (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Indica se esta forma pode dividir formas que sejam divisíveis.
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423556"
---
# <a name="shapesplit-cell-shape-layout-section"></a>Célula ShapeSplit (Seção Shape Layout)

Indica se esta forma pode dividir formas que sejam divisíveis.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Não permitir que esta forma divida outras formas.  <br/> |**visSLOSplitNone** <br/> |
| 1   <br/> | Permitir que esta forma divida outras formas.  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Comentários

Uma forma que divide outras formas deve ser uma forma 2D ou uma forma de colocação 1D. 
  
A divisão automática de formas é habilitada e desabilitada em três níveis diferentes: aplicativo, página e forma. Por padrão, a divisão é habilitada no nível do aplicativo e da página; nas formas, ela varia por tipo de desenho. 
  
Para habilitar ou desabilitar a  divisão no nível do aplicativo, use a configuração  de divisão do conector Habilitar na guia Avançado da caixa de diálogo Opções do **Visio** (clique na guia Arquivo, clique em Opções e em  **Avançado).** 
  
Para habilitar ou desabilitar a divisão em uma página, consulte a célula PageShapeSplit. 
  
Para fazer com que uma forma 1D possa ser dividida, consulte a célula ShapeSplittable.
  
Para fazer referência à célula ShapeSplit pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShapeSplit  <br/> |
   
Para fazer referência à célula ShapeSplit pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
| Índice de célula:  <br/> |**visSLOSplit** <br/> |
   

