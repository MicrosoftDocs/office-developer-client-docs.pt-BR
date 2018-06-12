---
title: Célula WalkPreference (Seção Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Determina se um ponto de extremidade de uma forma 1D será movido para um ponto de conexão horizontal ou vertical na forma à qual está colado, usando a cola dinâmica, quando a forma for movida para uma posição ambígua. Como padrão, ambos os pontos de extremidade da forma 1D são movidos para pontos de conexão horizontais.
ms.openlocfilehash: cd64a67de6ec914ad1bde86cdac829f6c12cebe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773273"
---
# <a name="walkpreference-cell-glue-info-section"></a>Célula WalkPreference (Seção Glue Info)

Determina se um ponto de extremidade de uma forma 1D será movido para um ponto de conexão horizontal ou vertical na forma à qual está colado, usando a cola dinâmica, quando a forma for movida para uma posição ambígua. Como padrão, ambos os pontos de extremidade da forma 1D são movidos para pontos de conexão horizontais.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 1  <br/> | O ponto inicial da forma 1D é movido para um ponto de conexão vertical e o ponto de extremidade é movido para um ponto de conexão horizontal (conexões de cima para o lado ou de baixo para o lado).  <br/> |**visWalkPrefBegNS** <br/> |
| 2  <br/> | O ponto inicial da forma 1D é movido para um ponto de conexão horizontal e o ponto final é movido para um ponto de conexão vertical (conexões do lado para cima ou do lado para baixo).  <br/> |**visWalkPrefEndNS** <br/> |
   
## <a name="remarks"></a>Comentários

Esta célula não tem efeito em conectores dinâmicos. Um comportamento de um conector dinâmico é determinado pelo seu estilo de roteamento. Verifique a célula RouteStyle para obter o estilo de roteamento padrão para conectores dinâmicos em uma página ou a célula ShapeRouteStyle para obter o estilo de roteamento de um determinado conector dinâmico.
  
Para obter uma referência à célula WalkPreference pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | WalkPreference  <br/> |
   
Para obter uma referência à célula WalkPreference pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visWalkPref** <br/> |
   

