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
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406539"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>Célula TextBkgnd (Seção Text Block Format)

Determina a cor do plano de fundo do texto de uma forma.
  
## <a name="remarks"></a>Comentários

A célula TextBkgnd pode ter qualquer valor de 0 até 24 ou 255. Os valores 0 e 255 ( *visTxtBlklOpaque*) indicam um plano de fundo de texto transparente. 
  
Para inserir uma cor personalizada, utilize a função RGB ou HSL mais um, como, por exemplo, RGB(255,127,255)+1. O valor de uma cor personalizada é sua cor RGB, e RGB( *r, g, b*)+1, em vez de um número, será mostrado na janela ShapeSheet. Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 25. 
  
É possível definir a transparência da cor do plano de fundo do texto na célula TextBkgndTrans.
  
Para obter uma referência para a célula TextBkgnd pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |TextBkgnd  <br/> |
   
Para obter uma referência para a célula TextBkgnd pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowText** <br/> |
|Índice da célula:  <br/> |**visTxtBlkBkgnd** <br/> |
   

