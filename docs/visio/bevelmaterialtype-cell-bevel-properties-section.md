---
title: Célula BevelMaterialType (Seção Bevel Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: Determina o tipo de material do qual o bevel é composto.
ms.openlocfilehash: b8efaa1f84594c803c79be02cd88dda1a5346dc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414582"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a>Célula BevelMaterialType (Seção Bevel Properties)

Determina o tipo de material do qual o bevel é composto. 
  
|**Descrição**|**Valor**|
|:-----|:-----|
|0  <br/> |Nenhum material especial  <br/> |
|1   <br/> |Fosco  <br/> |
|2   <br/> |Mate Quente  <br/> |
|3   <br/> |Plástico  <br/> |
|4   <br/> |Metal  <br/> |
|5   <br/> |Borda Escura  <br/> |
|6   <br/> |Borda Suave  <br/> |
|7   <br/> |Plano  <br/> |
|8   <br/> |Estrutura  <br/> |
|9   <br/> |Pó  <br/> |
|10   <br/> |Pó Translúcido  <br/> |
|11  <br/> |Limpar  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **BevelMaterialType** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | BevelMaterialType  <br/> |
   
Para fazer referência à célula **BevelMaterialType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowBevelProperties** <br/> |
| Índice de célula:  <br/> |**visBevelMaterialType** <br/> |
   

