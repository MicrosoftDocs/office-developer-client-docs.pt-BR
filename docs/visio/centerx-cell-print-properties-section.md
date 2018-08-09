---
title: Célula CenterX (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Determina se a página de desenho ficará centralizada horizontalmente na página impressa.
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771493"
---
# <a name="centerx-cell-print-properties-section"></a>Célula CenterX (Seção Print Properties)

Determina se a página de desenho ficará centralizada horizontalmente na página impressa. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Centraliza a página de desenho horizontalmente na página impressa.  <br/> |
| FALSO  <br/> | Não centraliza a página de desenho horizontalmente na página impressa (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Por padrão, as páginas de desenho são justificadas ao alto e à esquerda da página impressa. A configuração das células CenterX e CenterY como VERDADEIRO coloca a página de desenho no centro da página impressa (ou páginas quando for necessário colocar lado a lado). 
  
Para fazer referência à célula CenterX pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | CenterX  <br/> |
   
Para fazer referência à célula CenterX pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesCenterX** <br/> |
   

