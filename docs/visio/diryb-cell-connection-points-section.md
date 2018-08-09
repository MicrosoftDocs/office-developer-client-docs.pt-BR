---
title: Célula DirY / B (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Determina a y-component necessários vetor de alinhamento de um ponto de conexão coincidente. Ele também é usado para orientar o segmento anexado de um conector dinâmico. Essa célula assume uma flutuante valor de ponto.
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771709"
---
# <a name="diry--b-cell-connection-points-section"></a>Célula DirY / B (Seção Connection Points)

Determina a *y* -component necessários vetor de alinhamento de um ponto de conexão coincidente. Ele também é usado para orientar o segmento anexado de um conector dinâmico. Essa célula assume uma flutuante valor de ponto. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula DirY / B pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Connections.DirY [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula DirY / B pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
|Índice da linha:  <br/> |**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCnnctDirY** (linhas não-estendidas)           **visCnnctB** (linhas estendidas)  <br/> |
   
Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.
  

