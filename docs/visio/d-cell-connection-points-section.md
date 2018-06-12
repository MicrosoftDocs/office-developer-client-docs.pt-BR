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
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771642"
---
# <a name="d-cell-connection-points-section"></a>Célula D (Seção Connection Points)

Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.
  
## <a name="remarks"></a>Comentários

Para acessar a célula D, do mouse em uma linha e clique em **Alterar tipo de linha** no menu de atalho. 
  
Para obter uma referência à célula D pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Connections.D [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula D pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
| Índice da linha:  <br/> |**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCnnctD** <br/> |
   

