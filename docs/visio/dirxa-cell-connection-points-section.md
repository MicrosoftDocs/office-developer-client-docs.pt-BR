---
title: Célula DirX / A (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Determina o componente x para o vetor de alinhamento obrigatório de um ponto de conexão correspondente. A célula DirX / A é também utilizada para orientar o segmento anexado de um conector dinâmico. Essa célula assume um valor de ponto flutuante.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422394"
---
# <a name="dirx--a-cell-connection-points-section"></a>Célula DirX / A (Seção Connection Points)

Determina o componente *x* para o vetor de alinhamento obrigatório de um ponto de conexão correspondente. A célula DirX / A é também utilizada para orientar o segmento anexado de um conector dinâmico. Essa célula assume um valor de ponto flutuante. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula DirX / A pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Connections. célula Dirx [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula DirX / A pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
| Índice de linha:  <br/> |**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2  <br/> |
| Índice da célula:  <br/> |**visCnnctDirX** (linhas não estendidas)           **visCnnctA** (linhas estendidas)  <br/> |
   
Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.
  

