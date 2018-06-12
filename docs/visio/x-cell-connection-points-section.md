---
title: Célula X (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Representa o x-coordenadas de um ponto de conexão em coordenadas locais.
ms.openlocfilehash: 27821f9aa94f97d8e019d7c7307c036549bf807b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773297"
---
# <a name="x-cell-connection-points-section"></a>Célula X (Seção Connection Points)

Representa o *x* -coordenadas de um ponto de conexão em coordenadas locais. 
  
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula X pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Connections.X *i* onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula X pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
| Índice da linha:  <br/> |**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visX** <br/> |
   

