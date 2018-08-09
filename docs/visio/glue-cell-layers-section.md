---
title: Célula Glue (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Especifica se as formas pertencentes à camada podem ser coladas.
ms.openlocfilehash: 81a54bebaa8ca68a8fbc8853c69f88efb34bbdb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771963"
---
# <a name="glue-cell-layers-section"></a>Célula Glue (Seção Layers)

Especifica se as formas pertencentes à camada podem ser coladas.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A cola está ativada.  <br/> |
|FALSO  <br/> |A cola não está ativada.  <br/> |
   
## <a name="remarks"></a>Comentários

Essa célula corresponde à opção **associar** na caixa de diálogo **Propriedades da camada** (na guia **página inicial** , no grupo **edição** , clique em **camadas**e, em seguida, clique em **Propriedades da camada** ). 
  
Para obter uma referência para a célula Glue pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers.Glue [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência para a célula Glue pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice da linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visLayerGlue** <br/> |
   

