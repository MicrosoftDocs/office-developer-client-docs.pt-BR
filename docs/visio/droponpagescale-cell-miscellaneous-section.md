---
title: Célula DropOnPageScale (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423759"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>Célula DropOnPageScale (Seção Diversos)

Contém o percentual da escala de uma forma quando colocada na página de desenho.
  
## <a name="remarks"></a>Comentários

Nos seguintes casos, o Visio coloca as formas em escala para que apareçam adequadamente na página de desenho:
  
- Quando formas sem medida são colocadas em desenhos com escala.
    
- Quando as formas medidas são colocadas em desenhos não dimensionados.
    
A porcentagem na célula DropOnPageScale indica o fator pelo qual o Visio escalou a forma, seja para cima (\>100) ou para baixo (\<100). Você pode usar esse número como um fator ao calcular valores codificados. 
  
Esse valor é 100% para formas com medida em desenhos com escala ou formas sem medida em desenhos sem escala. 
  
Para fazer referência à célula DropOnPageScale pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DropOnPageScale  <br/> |
   
Para fazer referência à célula DropOnPageScale pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowMisc** <br/> |
| Índice de célula:  <br/> |**visObjDropOnPageScale** <br/> |
   

