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
ms.openlocfilehash: 0624ec42978292e84965c978d25e4052fc41613f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772755"
---
# <a name="rounding-cell-line-format-section"></a>Célula Rounding (Seção Line Format)

Indica o raio do arco de arredondamento aplicado onde dois segmentos contíguos de um caminho se encontram. Por exemplo, o arredondamento pode ser utilizado nos cantos de um retângulo. Para definir o arredondamento, insira um valor com unidades de medida (um par de unidades numéricas).
  
## <a name="remarks"></a>Comentários

Você também pode definir esse valor na caixa de diálogo **linha** (na guia **página inicial** , no grupo **forma** , clique em **linha**, aponte para **espessura**e, em seguida, clique em **Mais linhas**).
  
Para obter uma referência para a célula Rounding pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Rounding  <br/> |
   
Para obter uma referência para a célula Rounding pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLine** <br/> |
|Índice da célula:  <br/> |**visLineRounding** <br/> |
   

