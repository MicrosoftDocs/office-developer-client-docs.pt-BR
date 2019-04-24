---
title: Célula ShapeShdwShow (seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Determina se a forma exibe uma sombra, como um inteiro de 0 a 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349144"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>Célula ShapeShdwShow (seção Fill Format)

Determina se a forma exibe uma sombra, como um inteiro de 0 a 2.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |Sempre exibe a sombra se for especificada uma sombra. As sombras de subformas não são exibidas.  <br/> |
|1  <br/> |Não processa uma sombra, a menos que a forma não tenha um pai. Use as sombras de subformas, se agrupadas.  <br/> |
|duas  <br/> |Sempre exibe uma sombra se uma sombra é especificada. As sombras das subformas são exibidas.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **ShapeShdwShow** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShapeShdwShow  <br/> |
   
Para obter uma referência para a célula **ShapeShdwShow** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowFill** <br/> |
| Índice da célula:  <br/> |**visFillShdwShow** <br/> |
   

