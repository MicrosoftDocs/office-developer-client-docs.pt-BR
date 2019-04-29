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
ms.openlocfilehash: 13b05ed71248a3f8fada947fca6b203c6ab19c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418075"
---
# <a name="centerx-cell-print-properties-section"></a>Célula CenterX (Seção Print Properties)

Determina se a página de desenho ficará centralizada horizontalmente na página impressa. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Centraliza a página de desenho horizontalmente na página impressa.  <br/> |
| FALSE  <br/> | Não centraliza a página de desenho horizontalmente na página impressa (o padrão).  <br/> |
   
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
| Índice de linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesCenterX** <br/> |
   

