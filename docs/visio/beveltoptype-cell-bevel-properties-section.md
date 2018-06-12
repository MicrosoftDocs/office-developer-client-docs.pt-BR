---
title: Célula BevelTopType (seção Propriedades de bisel)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e29af0d-4183-41d1-8b0f-96450089f882
description: Determina o tipo de bisel na borda superior de uma forma.
ms.openlocfilehash: 6fea6f119e4948634edf8fd1fc22b2fd6e7675d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771324"
---
# <a name="beveltoptype-cell-bevel-properties-section"></a>Célula BevelTopType (seção Propriedades de bisel)

Determina o tipo de bisel na borda superior de uma forma. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Nenhum bisel  <br/> |
|1  <br/> |Bisel círculo  <br/> |
|2  <br/> |Bisel de baixo-relevo Relaxado  <br/> |
|3  <br/> |Bisel cruz  <br/> |
|4  <br/> |Bisel de inclinação interessante  <br/> |
|5  <br/> |Bisel ângulo  <br/> |
|6  <br/> |Arredondar suave bisel  <br/> |
|7  <br/> |Bisel convexo  <br/> |
|8  <br/> |Bisel inclinação  <br/> |
|9  <br/> |Bisel malha  <br/> |
|10  <br/> |Bisel talho  <br/> |
|11  <br/> |Disco rígido bisel de borda  <br/> |
|12  <br/> |Bisel art decô  <br/> |
   
## <a name="remarks"></a>Coment�rios

Para fazer referência à célula **BevelTopType** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |BevelTopType  <br/> |
   
Para obter uma referência à célula **BevelTopType** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowBevelProperties** <br/> |
|Índice da célula:  <br/> |**visBevelTopType** <br/> |
   

