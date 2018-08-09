---
title: Célula PageBottomMargin (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Especifica a margem inferior da página.
ms.openlocfilehash: fb67cf87f5e50719d24b0f354acc93209eed8811
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772444"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>Célula PageBottomMargin (Seção Print Properties)

Especifica a margem inferior da página.
  
## <a name="remarks"></a>Comentários

Esse valor representa unidades físicas e não é afetado pelas unidades de escala ou de desenho. Por exemplo, se o valor dessa célula for 0,5 pol., essa margem será 0,5 polegadas, mesmo que as unidades da página sejam pés. Se as unidades não estiverem explicitamente definidas, o valor utilizado como padrão são as unidades da página. 
  
Para fazer referência à célula PageBottomMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageBottomMargin  <br/> |
   
Para fazer referência à célula PageBottomMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesBottomMargin** <br/> |
   

