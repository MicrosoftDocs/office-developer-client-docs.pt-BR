---
title: Célula LineColor (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Determina a cor da linha da forma.
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772197"
---
# <a name="linecolor-cell-line-format-section"></a>Célula LineColor (Seção Line Format)

Determina a cor da linha da forma.
  
## <a name="remarks"></a>Comentários

Para definir a cor da linha, insira um número de 0 a 23, que é um índice em uma coleção de cores de linha. Você pode visualizar a coleção de cor de linha na caixa de diálogo **linha** (na guia **página inicial** , no grupo **forma** , clique em **linha**, aponte para **espessura**e, em seguida, clique em **Mais linhas**). Você também pode definir o valor da célula LineColor na caixa de diálogo **linha** . 
  
Para inserir uma cor personalizada, use a função RGB ou HSL. O valor de uma cor personalizada é a cor RGB e RGB ( *r, g, b*), em vez de um número, será exibido na janela ShapeSheet. Quando usado em operações numéricas, as cores têm valores de 24 e acima. 
  
É possível definir a transparência da cor de linha na célula LineColorTrans.
  
Para obter uma referência para a célula LineColor pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineColor  <br/> |
   
Para obter uma referência para a célula LineColor pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLine** <br/> |
|Índice da célula:  <br/> |**visLineColor** <br/> |
   

