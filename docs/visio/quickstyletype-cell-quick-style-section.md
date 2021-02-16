---
title: Célula QuickStyleType (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina o tipo de Estilo Rápido (bidimensional, unidimensional ou conector) que a forma herda.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410501"
---
# <a name="quickstyletype-cell-quick-style-section"></a>Célula QuickStyleType (Seção Quick Style)

Determina o tipo de Estilo Rápido (bidimensional, unidimensional ou conector) que a forma herda. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |O Visio escolhe automaticamente  <br/> |
|1   <br/> |Unidimensional  <br/> |
|2   <br/> |Bidimensional  <br/> |
|3   <br/> |Connector  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **QuickStyleType** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | QuickStyleType  <br/> |
   
Para fazer referência à **célula QuickStyleType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice de célula:  <br/> |**visQuickStyleType** <br/> |
   

