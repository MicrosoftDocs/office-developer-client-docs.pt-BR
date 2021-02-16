---
title: Célula DocLockDuplicatePage (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Determina se as páginas no documento podem ser duplicadas, como um Boolean.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439657"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>Célula DocLockDuplicatePage (Seção Document Properties)

Determina se as páginas no documento podem ser duplicadas, como um Boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |**A** duplicação no menu de atalho de página e o método de automação **Page.Duplicate** estão desabilitados.  <br/> |
|FALSE  <br/> |A página pode ser duplicada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **DocLockDuplicatePage** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DocLockDuplicatePage  <br/> |
   
Para fazer referência à **célula DocLockDuplicatePage** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowDoc** <br/> |
| Índice de célula:  <br/> |**visDocLockDuplicatePage** <br/> |
   

