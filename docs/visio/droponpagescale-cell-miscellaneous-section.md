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
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771764"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>Célula DropOnPageScale (Seção Miscellaneous)

Contém o percentual da escala de uma forma quando colocada na página de desenho.
  
## <a name="remarks"></a>Comentários

Nos seguintes casos, o Visio coloca as formas em escala para que apareçam adequadamente na página de desenho:
  
- Quando formas sem medida são colocadas em desenhos com escala.
    
- Quando formas com medida são colocadas em desenhos sem escala.
    
O percentual da célula DropOnPageScale indica o fator pelo qual o Visio dimensionado de forma, acima (\>100) ou para baixo (\<100). Você pode usar esse número como um fator ao calcular valores codificados. 
  
Esse valor é 100% para formas com medida em desenhos com escala ou formas sem medida em desenhos sem escala. 
  
Para obter uma referência à célula DropOnPageScale pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DropOnPageScale  <br/> |
   
Para obter uma referência à célula DropOnPageScale pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visObjDropOnPageScale** <br/> |
   

