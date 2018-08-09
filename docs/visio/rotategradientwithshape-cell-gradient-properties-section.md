---
title: Célula RotateGradientWithShape (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Determina se um gradiente do preenchimento gira com a forma em rotação 2D, como um valor booleano.
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772734"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>Célula RotateGradientWithShape (Seção Gradient Properties)

Determina se um gradiente do preenchimento gira com a forma em rotação 2D, como um valor booleano.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Gradiente gira com a forma quando a forma for girada ao redor do pino rotação. O "superior" do gradiente é paralelo com a alça de rotação.  <br/> |
|FALSO  <br/> |Gradiente não gira com a forma quando a forma for girada ao redor do pino rotação. O "superior" do gradiente é paralelo à tela de desenho.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **RotateGradientWithShape** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | RotateGradientWithShape  <br/> |
   
Para obter uma referência à célula **RotateGradientWithShape** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |**visRotateGradientWithShape** <br/> |
   

