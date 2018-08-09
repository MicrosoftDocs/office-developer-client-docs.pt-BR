---
title: Célula CompoundType (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Determina o tipo de compostos da linha de uma forma.
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771546"
---
# <a name="compoundtype-cell-line-format-section"></a>Célula CompoundType (Seção Line Format)

Determina o tipo de compostos da linha de uma forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Simples  <br/> |
|1  <br/> |Double  <br/> |
|2  <br/> |Espessura finas  <br/> |
|3  <br/> |Grossa fina  <br/> |
|4  <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **CompoundType** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | CompoundType  <br/> |
   
Para obter uma referência à célula **CompoundType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLine** <br/> |
| Índice da célula:  <br/> |**visCompoundType** <br/> |
   

