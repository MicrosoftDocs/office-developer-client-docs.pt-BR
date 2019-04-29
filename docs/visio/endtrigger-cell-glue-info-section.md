---
title: Célula EndTrigger (Seção Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251331
localization_priority: Normal
ms.assetid: 8dc6515b-66ab-f1ac-18fd-820209f90991
description: Contém uma fórmula de gatilho gerada pelo aplicativo que determina se o ponto final de uma forma 1-D deve ser movido para manter sua conexão com outra forma.
ms.openlocfilehash: 9093cca782d9262b2511198ed73f512a75bb8994
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418579"
---
# <a name="endtrigger-cell-glue-info-section"></a>Célula EndTrigger (Seção Glue Info)

Contém uma fórmula de gatilho gerada pelo aplicativo que determina se o ponto final de uma forma 1-D deve ser movido para manter sua conexão com outra forma.
  
## <a name="remarks"></a>Comentários

Ao associar uma forma 1D a outra usando a associação dinâmica, o Visio gera uma fórmula que faz referência à célula EventXFMod da outra forma. Quando a forma 1D é alterada, o Visio recalcula todas as fórmulas que fazem referência a sua célula EventXFMod, incluindo a fórmula na célula EndTrigger. Outras fórmulas da forma 1D fazem referência à célula EndTrigger e movem o ponto final da forma 1D ou alteram a forma conforme necessário.
  
Para fazer referência à célula EndTrigger pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | EndTrigger  <br/> |
   
Para fazer referência à célula EndTrigger pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowMisc** <br/> |
| Índice de célula:  <br/> |**visEndTrigger** <br/> |
   

