---
title: Célula PageLockDuplicate (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina se a página pode ser duplicada, como um valor booleano.
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772450"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>Célula PageLockDuplicate (Seção Page Properties)

Determina se a página pode ser duplicada, como um valor booleano.
  
|||
|:-----|:-----|
|VERDADEIRO  <br/> |**Duplicar** no menu de atalho de página e o método de automação **Page.Duplicate** estão ambos desabilitados para a página.  <br/> |
|FALSO  <br/> |A página pode ser duplicada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **PageLockDuplicate** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageLockDuplicate  <br/> |
   
Para obter uma referência à célula **PageLockDuplicate** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageLockDuplicate** <br/> |
   

