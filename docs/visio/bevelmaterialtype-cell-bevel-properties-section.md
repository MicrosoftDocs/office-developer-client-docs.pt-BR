---
title: Célula BevelMaterialType (Seção Bevel Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: Determina o tipo de bisel é composto de material.
ms.openlocfilehash: cd4ab223754ffcf7f46478cbc65faff373a3d692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771328"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a>Célula BevelMaterialType (Seção Bevel Properties)

Determina o tipo de bisel é composto de material. 
  
|**Descrição**|**Valor**|
|:-----|:-----|
|0  <br/> |Nenhum material especial  <br/> |
|1  <br/> |Fosco  <br/> |
|2  <br/> |Mate Quente  <br/> |
|3  <br/> |Plástico  <br/> |
|4  <br/> |Metal  <br/> |
|5  <br/> |Borda escura  <br/> |
|6  <br/> |Borda Suave  <br/> |
|7  <br/> |Plano  <br/> |
|8  <br/> |Estrutura  <br/> |
|9  <br/> |Pó  <br/> |
|10  <br/> |Pó Translúcido  <br/> |
|11  <br/> |Limpar  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **BevelMaterialType** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | BevelMaterialType  <br/> |
   
Para obter uma referência à célula **BevelMaterialType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowBevelProperties** <br/> |
| Índice da célula:  <br/> |**visBevelMaterialType** <br/> |
   

