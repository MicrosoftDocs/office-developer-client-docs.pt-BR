---
title: Célula D (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.
ms.openlocfilehash: e7bd61b8bc7a1a3b765af738681d958e2c83ba05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408170"
---
# <a name="d-cell-connection-points-section"></a>Célula D (Seção Connection Points)

Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.
  
## <a name="remarks"></a>Comentários

Para acessar a célula D, clique com o botão direito do mouse em uma linha e clique em **Alterar tipo de linha** no menu de atalho. 
  
Para fazer referência à célula D pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Connections. D [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula D pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
| Índice de linha:  <br/> |**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCnnctD** <br/> |
   

