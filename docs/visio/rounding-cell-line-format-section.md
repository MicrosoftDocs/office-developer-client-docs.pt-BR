---
title: Célula Rounding (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Indica o raio do arco de arredondamento aplicado onde dois segmentos contíguos de um caminho se encontram. Por exemplo, o arredondamento pode ser utilizado nos cantos de um retângulo. Para definir o arredondamento, insira um valor com unidades de medida (um par de unidades numéricas).
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427007"
---
# <a name="rounding-cell-line-format-section"></a>Célula Rounding (Seção Line Format)

Indica o raio do arco de arredondamento aplicado onde dois segmentos contíguos de um caminho se encontram. Por exemplo, o arredondamento pode ser utilizado nos cantos de um retângulo. Para definir o arredondamento, insira um valor com unidades de medida (um par de unidades numéricas).
  
## <a name="remarks"></a>Comentários

Você também pode definir esse valor na caixa de diálogo **linha** (na guia **página inicial** , no grupo **forma** , clique em **linha**, aponte para **espessura**e clique em **mais linhas**).
  
Para obter uma referência para a célula Rounding pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Arredondamento  <br/> |
   
Para obter uma referência para a célula Rounding pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowLine** <br/> |
|Índice de célula:  <br/> |**visLineRounding** <br/> |
   

