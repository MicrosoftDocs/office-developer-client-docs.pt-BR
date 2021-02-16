---
title: Célula FillForegnd (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Determina a cor usada para o primeiro plano (traço) do padrão de preenchimento da forma.
ms.openlocfilehash: 352fecf8d99069cfb5ebd72d295284dc03446364
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415562"
---
# <a name="fillforegnd-cell-fill-format-section"></a>Célula FillForegnd (Seção Fill Format)

Determina a cor usada para o primeiro plano (traço) do padrão de preenchimento da forma.
  
## <a name="remarks"></a>Comentários

Para definir a cor, insira um número de 0 a 23.
  
Para inserir uma cor personalizada, utilize a função RGB ou HSL. O valor de uma cor personalizada é sua cor RGB, e RGB( *r, g, b*), em vez de um número, será mostrado na janela ShapeSheet. Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24. 
  
É possível definir a transparência de preenchimento do primeiro plano na célula FillForegndTrans.
  
Para obter uma referência para a célula FillForegnd pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |FillForegnd  <br/> |
   
Para obter uma referência para a célula FillForegnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowFill** <br/> |
|Índice de célula:  <br/> |**visFillForegnd** <br/> |
   

