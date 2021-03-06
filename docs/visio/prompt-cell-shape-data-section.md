---
title: Célula Prompt (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Especifica um texto descritivo ou de instruções que aparece como uma dica quando o mouse está pausado sobre um valor na janela Dados da Forma.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405482"
---
# <a name="prompt-cell-shape-data-section"></a>Célula Prompt (Seção Shape Data)

Especifica o texto descritivo ou instrucional exibido como uma dica ao posicionar o mouse sobre o valor na janela **Dados da Forma**. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Prompt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Prop.  *Nome*  . Prompt onde  *Name*  é o nome da linha  <br/> |
   
Para fazer referência à célula Prompt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice de linha:  <br/> |**visRowProp +** *i*  onde  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visCustPropsPrompt** <br/> |
   

