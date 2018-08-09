---
title: Célula DocLockDuplicatePage (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Determina se páginas no documento podem ser duplicadas, como um valor booleano.
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771739"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>Célula DocLockDuplicatePage (Seção Document Properties)

Determina se páginas no documento podem ser duplicadas, como um valor booleano.
  
|||
|:-----|:-----|
|VERDADEIRO  <br/> |**Duplicar** no menu de atalho de página e o método de automação **Page.Duplicate** estão desativados.  <br/> |
|FALSO  <br/> |A página pode ser duplicada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **DocLockDuplicatePage** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DocLockDuplicatePage  <br/> |
   
Para obter uma referência à célula **DocLockDuplicatePage** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowDoc** <br/> |
| Índice da célula:  <br/> |**visDocLockDuplicatePage** <br/> |
   

