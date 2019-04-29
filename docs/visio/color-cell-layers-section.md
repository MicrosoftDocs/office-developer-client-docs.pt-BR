---
title: Célula Color (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Especifica a cor usada para exibir a camada.
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435128"
---
# <a name="color-cell-layers-section"></a>Célula Color (Seção Layers)

Especifica a cor usada para exibir a camada.
  
## <a name="remarks"></a>Comentários

Para definir a cor, insira um número de 0 a 23.
  
O valor da célula corresponde à **configuração cor da camada** na caixa de diálogo Propriedades da **camada** (no grupo **edição** na guia **página inicial** , clique em **camadas** e em **Propriedades da camada**).
  
Para inserir uma cor personalizada, utilize a função RGB ou HSL. O valor de uma cor personalizada é sua cor RGB e RGB ( *r, g, b*), e não um número, serão mostrados na janela ShapeSheet. Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24. O valor 255 indica que a camada está sem cor. 
  
É possível definir a transparência da cor da camada na célula Transparency.
  
Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers. Color [ *i* ] onde *i* = <1>, 2, 3,...  <br/> |
   
Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice de linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2,...  <br/> |
|Índice da célula:  <br/> |**visLayerColor** <br/> |
   

