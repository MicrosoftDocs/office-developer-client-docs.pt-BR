---
title: Célula ShapeShdwShow (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina se a forma exibirá uma sombra, como um inteiro de 0 a 2.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772913"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>Célula ShapeShdwShow (Seção Fill Format)

Determina se a forma exibirá uma sombra, como um inteiro de 0 a 2.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Sempre exibe a sombra se uma sombra for especificada. As sombras para subformas não são exibidas.  <br/> |
|1  <br/> |Não processam uma sombra, a menos que a forma não tem um pai. Use sombras de forma sub-recurso se agrupadas.  <br/> |
|2  <br/> |Sempre exiba uma sombra se uma sombra for especificada. As sombras para subformas são exibidas.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **ShapeShdwShow** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShapeShdwShow  <br/> |
   
Para obter uma referência à célula **ShapeShdwShow** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowFill** <br/> |
| Índice da célula:  <br/> |**visFillShdwShow** <br/> |
   

