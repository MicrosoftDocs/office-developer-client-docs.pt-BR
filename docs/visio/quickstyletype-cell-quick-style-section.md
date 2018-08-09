---
title: Célula QuickStyleType (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina o tipo de estilos rápidos (dimensional-2, 1-dimensional, ou um conector) que herda a forma.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772629"
---
# <a name="quickstyletype-cell-quick-style-section"></a>Célula QuickStyleType (Seção Quick Style)

Determina o tipo de estilos rápidos (dimensional-2, 1-dimensional, ou um conector) que herda a forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |O Visio escolhe automaticamente  <br/> |
|1  <br/> |1-dimensional  <br/> |
|2  <br/> |2-dimensional  <br/> |
|3  <br/> |Conector  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **QuickStyleType** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | QuickStyleType  <br/> |
   
Para obter uma referência à célula **QuickStyleType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice da célula:  <br/> |**visQuickStyleType** <br/> |
   

