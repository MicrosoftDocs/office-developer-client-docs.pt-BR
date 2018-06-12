---
title: Célula SortKey (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Um número que determina a ordem de hiperlinks que aparecem em um menu de atalho.
ms.openlocfilehash: 03596918924b04a776eb7ffd2f16db1c57de8194
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773039"
---
# <a name="sortkey-cell-hyperlinks-section"></a>Célula SortKey (Seção Hyperlinks)

Um número que determina a ordem de hiperlinks que aparecem em um menu de atalho.
  
## <a name="remarks"></a>Comentários

Os hiperlinks de um menu de atalho são exibidos no menu classificados do mais baixo ao mais alto, com os números menores exibidos no alto do menu. Se duas linhas de hiperlink tiverem o mesmo valor na célula SortKey, a ordem é determinada por ordem de linha física. O padrão é 0 (zero). 
  
Para obter uma referência para a célula SortKey pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Hiperlink. *nome* . SortKey onde Hyperlink *. nome* é o nome da linha  <br/> |
   
Para obter uma referência para a célula SortKey pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionHyperlink** <br/> |
|Índice da linha:  <br/> |**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visHLinkSortKey** <br/> |
   

