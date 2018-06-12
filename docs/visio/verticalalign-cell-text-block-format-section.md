---
title: Célula VerticalAlign (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Determina o alinhamento vertical do texto no bloco de texto.
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773260"
---
# <a name="verticalalign-cell-text-block-format-section"></a>Célula VerticalAlign (Seção Text Block Format)

Determina o alinhamento vertical do texto no bloco de texto.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Superior  <br/> |**visVertTop** <br/> |
| 1  <br/> | Meio  <br/> |**visVertMiddle** <br/> |
| 2  <br/> | Inferior  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula VerticalAlign pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | VerticalAlign  <br/> |
   
Para obter uma referência à célula VerticalAlign pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowText** <br/> |
| Índice da célula:  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

