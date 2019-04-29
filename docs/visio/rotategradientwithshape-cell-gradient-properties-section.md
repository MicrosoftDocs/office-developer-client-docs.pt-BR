---
title: Célula RotateGradientWithShape (seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Determina se um gradiente de preenchimento gira com uma forma em rotação 2D, como um Boolean.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412216"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>Célula RotateGradientWithShape (seção Gradient Properties)

Determina se um gradiente de preenchimento gira com uma forma em rotação 2D, como um Boolean.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O gradiente gira com a forma quando a forma é girada ao redor do pino de rotação. O "topo" do gradiente é paralelo à alça de rotação.  <br/> |
|FALSE  <br/> |O gradiente não gira com a forma quando a forma é girada ao redor do pino de rotação. O "topo" do gradiente é paralelo à tela de desenho.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **RotateGradientWithShape** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | RotateGradientWithShape  <br/> |
   
Para obter uma referência para a célula **RotateGradientWithShape** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowGradientProperties** <br/> |
| Índice da célula:  <br/> |**visRotateGradientWithShape** <br/> |
   

