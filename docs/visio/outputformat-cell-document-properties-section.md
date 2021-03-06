---
title: Célula OutputFormat (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Determina o formato de saída do desenho. Normalmente, as páginas de desenho são formatadas para impressão (padrão); no entanto, é possível escolher outros formatos de saída.
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413882"
---
# <a name="outputformat-cell-document-properties-section"></a>Célula OutputFormat (Seção Document Properties)

Determina o formato de saída do desenho. Normalmente, as páginas de desenho são formatadas para impressão (padrão); no entanto, é possível escolher outros formatos de saída.
  
|**Valor**|**Formato de saída**|
|:-----|:-----|
| 0  <br/> | Impressão (padrão)  <br/> |
| 1   <br/> | Apresentação de slides do PowerPoint  <br/> |
| 2   <br/> | Saída HTML ou GIF  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula OutputFormat pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | OutputFormat  <br/> |
   
Para fazer referência à célula OutputFormat pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowDoc** <br/> |
| Índice da célula:  <br/> |**visDocOutputFormat** <br/> |
   

