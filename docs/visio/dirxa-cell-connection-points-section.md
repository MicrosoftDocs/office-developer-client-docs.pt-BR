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
description: Determina o x-component necessários vetor de alinhamento de um ponto de conexão coincidente. DirX / uma célula também é usada para orientar o segmento anexado de um conector dinâmico. Essa célula assume uma flutuante valor de ponto.
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771738"
---
# <a name="dirx--a-cell-connection-points-section"></a>Célula DirX / A (Seção Connection Points)

Determina o *x* -component necessários vetor de alinhamento de um ponto de conexão coincidente. DirX / uma célula também é usada para orientar o segmento anexado de um conector dinâmico. Essa célula assume uma flutuante valor de ponto. 
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula DirX / A pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Connections.DirX [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula DirX / A pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
| Índice da linha:  <br/> |**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2  <br/> |
| Índice da célula:  <br/> |**visCnnctDirX** (linhas não-estendidas)           **visCnnctA** (linhas estendidas)  <br/> |
   
Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.
  

