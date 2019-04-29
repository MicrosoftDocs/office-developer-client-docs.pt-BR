---
title: Célula PageLeftMargin (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Especifica a margem esquerda da página.
ms.openlocfilehash: 289bd0bf16c6dcd9b26ec1a8c7920a29dab724a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435667"
---
# <a name="pageleftmargin-cell-print-properties-section"></a>Célula PageLeftMargin (Seção Print Properties)

Especifica a margem esquerda da página.
  
## <a name="remarks"></a>Comentários

Esse valor representa unidades físicas e não é afetado pelas unidades de escala ou de desenho. Por exemplo, se o valor dessa célula for 0,25 pol., essa margem será 0,25 polegadas, mesmo que as unidades da página sejam pés. Se as unidades não estiverem explicitamente definidas, o valor utilizado como padrão são as unidades da página. 
  
Para fazer referência à célula PageLeftMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageLeftMargin  <br/> |
   
Para fazer referência à célula PageLeftMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesLeftMargin** <br/> |
   

