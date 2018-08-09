---
title: Célula UIFormat (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Determina o formato de um campo inserido em versões do Visio anteriores à versão Visio 2000.
ms.openlocfilehash: e9506404e8ccd6ae4452c10ecdcce2d4dfd7ac2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773232"
---
# <a name="uiformat-cell-text-fields-section"></a>Célula UIFormat (Seção Text Fields)

Determina o formato de um campo inserido em versões do Visio anteriores à versão Visio 2000.
  
## <a name="remarks"></a>Comentários

Esta célula não é exibida na janela ShapeSheet. Utilize essa célula se precisar lidar com questões de capacidade de compatibilidade com versões anteriores, como salvar um desenho do Visio 2000 em um formato de arquivo do Visio 5.0.
  
Para fazer referência à célula UIFormat pelo nome, a partir de outra fórmula ou programa que usa a propriedade **Cells**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Fields.UIFmt [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para fazer referência à célula UIFormat pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionTextField** <br/> |
| Índice da linha:  <br/> |**visRowField** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visFieldUIFormat** <br/> |
   

