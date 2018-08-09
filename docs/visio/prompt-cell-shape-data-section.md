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
description: Especifica o texto descritivo ou instrucional exibido como uma dica ao posicionar o mouse sobre o valor na janela Dados da Forma.
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772601"
---
# <a name="prompt-cell-shape-data-section"></a>Célula Prompt (Seção Shape Data)

Especifica o texto descritivo ou instrucional exibido como uma dica ao posicionar o mouse sobre o valor na janela **Dados da Forma**. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Prompt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Prop.  *Nome* . Onde *nome* é o nome da linha de prompt  <br/> |
   
Para fazer referência à célula Prompt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice da linha:  <br/> |**visRowProp +** *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCustPropsPrompt** <br/> |
   

