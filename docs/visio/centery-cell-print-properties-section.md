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
ms.openlocfilehash: 858bf41c74fdcbd82d271a379df7c5816a7796fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341913"
---
# <a name="centery-cell-print-properties-section"></a>Célula CenterY (Seção Print Properties)

Determina se a página de desenho ficará centralizada verticalmente na página impressa. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | Centraliza a página de desenho verticalmente na página impressa.  <br/> |
| FALSE  <br/> | Não centraliza a página de desenho verticalmente na página impressa (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Por padrão, as páginas de desenho são justificadas ao alto e à esquerda da página impressa. A configuração das células CenterX e CenterY como VERDADEIRO coloca a página de desenho no centro da página impressa (ou páginas quando for necessário colocar lado a lado). 
  
Para fazer referência à célula CenterY pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Centro  <br/> |
   
Para fazer referência à célula CenterY pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
| Índice da célula:  <br/> |**visPrintPropertiesCenterY** <br/> |
   

