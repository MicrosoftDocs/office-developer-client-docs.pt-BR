---
title: Célula BevelBottomType (Seção Bevel Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ac7b39d4-3942-4b23-b188-2c3f69e54929
description: Especifica o tipo de bevel inferior do bevel de uma forma.
ms.openlocfilehash: 0cd360f633145c7dea95438ffe2bc746e519ce13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431747"
---
# <a name="bevelbottomtype-cell-bevel-properties-section"></a>Célula BevelBottomType (Seção Bevel Properties)

Especifica o tipo de bevel inferior do bevel de uma forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Sem bevel  <br/> |
|1   <br/> |Bevel circle  <br/> |
|2   <br/> |Bevel Desconjunto Descontraído  <br/> |
|3   <br/> |Bevel cruzado  <br/> |
|4   <br/> |Bevel Cool Slant  <br/> |
|5   <br/> |Ângulo de bevel  <br/> |
|6   <br/> |Bevel Round Suave  <br/> |
|7   <br/> |Bevel convexo  <br/> |
|8   <br/> |Nível de inclinação  <br/> |
|9   <br/> |Nível divot  <br/> |
|10   <br/> |Bevel de costelet  <br/> |
|11  <br/> |Nível de borda rígido  <br/> |
|12   <br/> |Bevel Art Deco  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **BevelBottomType** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** no formato de arquivo .vsdx ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | BevelBottomType  <br/> |
   
Para fazer referência à célula **BevelBottomType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowBevelProperties** <br/> |
| Índice de célula:  <br/> |**visBevelBottomType** <br/> |
   

