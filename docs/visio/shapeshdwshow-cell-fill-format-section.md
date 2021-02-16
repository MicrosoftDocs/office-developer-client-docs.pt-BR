---
title: Célula ShapeShdwShow (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina se a forma exibirá uma sombra, como um inteiro de 0 a 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422114"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>Célula ShapeShdwShow (Seção Fill Format)

Determina se a forma exibirá uma sombra, como um inteiro de 0 a 2.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Sempre exibir a sombra se uma sombra for especificada. As sombras de sub formas não são exibidas.  <br/> |
|1   <br/> |Não renderizar uma sombra, a menos que a forma não tenha um pai. Use sombras de sub shape se agrupadas.  <br/> |
|2   <br/> |Sempre exibirá uma sombra se uma sombra for especificada. As sombras de sub formas são exibidas.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **ShapeShdwShow** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShapeShdwShow  <br/> |
   
Para fazer referência à **célula ShapeShdwShow** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowFill** <br/> |
| Índice de célula:  <br/> |**visFillShdwShow** <br/> |
   

