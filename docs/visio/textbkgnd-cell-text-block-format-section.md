---
title: Célula TextBkgnd (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Determina a cor do plano de fundo do texto de uma forma.
ms.openlocfilehash: 2256a4c89812924af820c020c225f4b82b1d4856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773133"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>Célula TextBkgnd (Seção Text Block Format)

Determina a cor do plano de fundo do texto de uma forma.
  
## <a name="remarks"></a>Comentários

A célula TextBkgnd pode ter qualquer valor de 0 a 24 ou 255. Os valores 0 e 255 ( *visTxtBlklOpaque*) indicam um plano de fundo do texto transparente. 
  
Para inserir uma cor personalizada, use a função RGB ou HSL mais um — por exemplo, RGB (255,127,255) + 1. O valor de uma cor personalizada é a cor RGB e RGB ( *r, g, b*) + 1, em vez de um número, será exibido na janela ShapeSheet. Quando usado em operações numéricas, as cores têm valores de 25 e acima. 
  
É possível definir a transparência da cor do plano de fundo do texto na célula TextBkgndTrans.
  
Para obter uma referência para a célula TextBkgnd pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |TextBkgnd  <br/> |
   
Para obter uma referência para a célula TextBkgnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowText** <br/> |
|Índice da célula:  <br/> |**visTxtBlkBkgnd** <br/> |
   

