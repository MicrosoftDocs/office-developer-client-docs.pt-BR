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
description: Determina o componente y para o vetor de alinhamento necessário de um ponto de conexão correspondente. Ela também é utilizada para orientar o segmento anexado de um conector dinâmico. Essa célula assume um valor de ponto flutuante.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417088"
---
# <a name="diry--b-cell-connection-points-section"></a>Célula DirY / B (Seção Connection Points)

Determina o componente  *y*  para o vetor de alinhamento necessário de um ponto de conexão correspondente. Ela também é utilizada para orientar o segmento anexado de um conector dinâmico. Essa célula assume um valor de ponto flutuante. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula DirY / B pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Connections.DirY[ *i*  ] onde  *i*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula DirY / B pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
|Índice de linha:  <br/> |**visRowConnectionPts**  +   *i* onde *i* = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visCnnctDirY** (linhas não estendidas)           **visCnnctB** (linhas estendidas)  <br/> |
   
Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.
  

