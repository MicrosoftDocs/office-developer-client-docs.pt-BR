---
title: Célula Snap (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Determina se outras formas podem ser ajustadas a formas atribuídas à camada. Formas atribuídas à camada podem ser ajustadas a outras formas, mas o contrário não ocorre.
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434841"
---
# <a name="snap-cell-layers-section"></a>Célula Snap (Seção Layers)

Determina se outras formas podem ser ajustadas a formas atribuídas à camada. Formas atribuídas à camada podem ser ajustadas a outras formas, mas o contrário não ocorre.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Outras formas podem ser ajustadas a formas na camada.  <br/> |
|FALSE  <br/> |Outras formas não podem ser ajustadas a formas na camada.  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o valor dessa célula usando a opção **Ajustar** na caixa de diálogo **Propriedades da Camada** (na guia **Página Inicial** no grupo **Edição** clique em **Camadas** e em **Propriedades da Camada**).
  
Para obter uma referência para a célula Snap pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers. snap [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Snap pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice de linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visLayerSnap** <br/> |
   

