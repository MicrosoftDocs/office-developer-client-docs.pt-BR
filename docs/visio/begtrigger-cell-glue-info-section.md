---
title: Célula BegTrigger (Seção Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
localization_priority: Normal
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: Contém uma fórmula de gatilho, gerada pelo aplicativo, que determina se o ponto inicial de uma forma 1D deve ser movido para manter sua conexão com outra forma.
ms.openlocfilehash: b401d349119337016a96b5fffbc26f7be2891864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437949"
---
# <a name="begtrigger-cell-glue-info-section"></a>Célula BegTrigger (Seção Informações de associação)

Contém uma fórmula de gatilho, gerada pelo aplicativo, que determina se o ponto inicial de uma forma 1D deve ser movido para manter sua conexão com outra forma.
  
## <a name="remarks"></a>Comentários

Ao associar uma forma 1D a outra usando a associação dinâmica, o aplicativo gera uma fórmula que faz referência à célula EventXFMod da outra forma. Quando a forma 1D é alterada, o Visio recalcula todas as fórmulas que fazem referência à célula EventXFMod, incluindo a fórmula na célula BegTrigger. Outras fórmulas da forma 1D fazem referência à célula BegTrigger e movem o ponto inicial da forma 1D ou alteram a forma conforme necessário.
  
Para fazer referência à célula BegTrigger pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | BegTrigger  <br/> |
   
Para fazer referência à célula BegTrigger pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowGroup** <br/> |
| Índice de célula:  <br/> |**visBegTrigger** <br/> |
   

