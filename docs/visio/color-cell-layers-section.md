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
ms.openlocfilehash: b6728d44c71f6403e772a6a7e730ba3c18d9eb48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771516"
---
# <a name="color-cell-layers-section"></a>Célula Color (Seção Layers)

Especifica a cor usada para exibir a camada.
  
## <a name="remarks"></a>Comentários

Para definir a cor, insira um número de 0 a 23.
  
Valor desta célula corresponde à configuração da **cor da camada** na caixa de diálogo **Propriedades da camada** (no grupo **edição** na guia **página inicial** , clique em **camadas** e, em seguida, clique em **Propriedades da camada**).
  
Para inserir uma cor personalizada, use a função RGB ou HSL. O valor de uma cor personalizada é a cor RGB e RGB ( *r, g, b*), em vez de um número, será exibido na janela ShapeSheet. Quando usado em operações numéricas, as cores têm valores de 24 e acima. Um valor de 255 indica que a camada está sem cor. 
  
É possível definir a transparência da cor da camada na célula Transparency.
  
Para fazer referência à célula Color pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers.Color [ *i* ] onde *i* = < 1 >, 2, 3,...  <br/> |
   
Para fazer referência à célula Color pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice da linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2,...  <br/> |
|Índice da célula:  <br/> |**visLayerColor** <br/> |
   

