---
title: Célula PageTopMargin (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
localization_priority: Normal
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Especifica a margem superior da página impressa.
ms.openlocfilehash: ff2bffffed39c5571386e792d2ffc8d20d6b291e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416577"
---
# <a name="pagetopmargin-cell-print-properties-section"></a>Célula PageTopMargin (Seção Print Properties)

Especifica a margem superior da página impressa.
  
## <a name="remarks"></a>Comentários

Esse valor representa unidades físicas e não é afetado pelas unidades de escala ou de desenho. Por exemplo, se o valor dessa célula for 0,25 pol., essa margem será 0,25 polegadas, mesmo que as unidades da página sejam pés. Se as unidades não estiverem explicitamente definidas, o valor utilizado como padrão são as unidades da página. 
  
Para fazer referência à célula PageTopMargin pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageTopMargin  <br/> |
   
Para fazer referência à célula PageTopMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesTopMargin** <br/> |
   

