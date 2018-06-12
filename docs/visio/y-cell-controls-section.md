---
title: Célula Y (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Representa o y-coordenada que indica a localização da alça de controle de uma forma em coordenadas locais.
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773322"
---
# <a name="y-cell-controls-section"></a>Célula Y (Seção Controls)

Representa o *y* -coordenada que indica a localização da alça de controle de uma forma em coordenadas locais. 
  
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula Y pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Controles.  *nome* . Controles de Ywhere.  *nome* é o nome da linha controles.  <br/> |
   
Para obter uma referência à célula Y pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionControls** <br/> |
| Índice da linha:  <br/> |**visRowControl** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCtlY** <br/> |
   

