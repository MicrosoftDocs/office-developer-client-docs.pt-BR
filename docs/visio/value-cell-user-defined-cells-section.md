---
title: Célula Value (Seção User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Especifica um valor para a célula definida pelo usuário correspondente.
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422984"
---
# <a name="value-cell-user-defined-cells-section"></a>Célula Value (Seção User-Defined Cells)

Especifica um valor para a célula definida pelo usuário correspondente.
  
## <a name="remarks"></a>Comentários

Para fazer referência a esse valor em outra célula, especifique o nome definido pelo usuário inserido no rótulo da linha User.Row.
  
Para fazer referência à célula Value pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Usuário.  *Nome*  . Valor em que Usuário.  *Name*  é o nome da linha  <br/> |
   
Para fazer referência à célula Value pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionUser** <br/> |
| Índice de linha:  <br/> |**visRowUser**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visUserValue** <br/> |
   

