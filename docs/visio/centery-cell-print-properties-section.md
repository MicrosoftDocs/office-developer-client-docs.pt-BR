---
title: Célula CenterY (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Determina se a página de desenho ficará centralizada verticalmente na página impressa.
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771512"
---
# <a name="centery-cell-print-properties-section"></a>Célula CenterY (Seção Print Properties)

Determina se a página de desenho ficará centralizada verticalmente na página impressa. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Centraliza a página de desenho verticalmente na página impressa.  <br/> |
| FALSO  <br/> | Não centraliza a página de desenho verticalmente na página impressa (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Por padrão, as páginas de desenho são justificadas ao alto e à esquerda da página impressa. A configuração das células CenterX e CenterY como VERDADEIRO coloca a página de desenho no centro da página impressa (ou páginas quando for necessário colocar lado a lado). 
  
Para fazer referência à célula CenterY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | CenterY  <br/> |
   
Para fazer referência à célula CenterY pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesCenterY** <br/> |
   

