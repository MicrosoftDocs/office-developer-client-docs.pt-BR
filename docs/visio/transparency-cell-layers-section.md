---
title: Célula Transparency (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Determina o nível de transparência para uma camada de cor.
ms.openlocfilehash: 7c205612436e7731f268e17c851616beebf809dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773174"
---
# <a name="transparency-cell-layers-section"></a>Célula Transparency (Seção Layers)

Determina o nível de transparência para uma camada de cor.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|
          0 - 100
  <br/> |Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma camada com cor completamente transparente tenha a mesma aparência de uma camada sem cor na página de desenho, ela interage com os outros objetos da página da mesma forma que se a transparência fosse 0%. Também é possível definir esse valor usando o controle deslizante na caixa de diálogo **Propriedades da Camada** (na guia **Página Inicial **, do grupo **Edição**, clique em **Camadas** e em **Propriedades da Camada**).
  
Para obter uma referência para a célula Transparency pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers.ColorTrans [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência para a célula Transparency pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice da linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visLayerColorTrans** <br/> |
   

