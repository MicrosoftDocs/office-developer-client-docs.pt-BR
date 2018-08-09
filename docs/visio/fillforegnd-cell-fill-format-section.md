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
ms.openlocfilehash: 27126457963e4e55419b0cac5baf1eab08fe3cc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771884"
---
# <a name="fillforegnd-cell-fill-format-section"></a>Célula FillForegnd (Seção Fill Format)

Determina a cor usada para o primeiro plano (traço) do padrão de preenchimento da forma.
  
## <a name="remarks"></a>Comentários

Para definir a cor, insira um número de 0 a 23.
  
Para inserir uma cor personalizada, use a função RGB ou HSL. O valor de uma cor personalizada é a cor RGB e RGB ( *r, g, b*), em vez de um número, será exibido na janela ShapeSheet. Quando usado em operações numéricas, as cores têm valores de 24 e acima. 
  
É possível definir a transparência de preenchimento do primeiro plano na célula FillForegndTrans.
  
Para obter uma referência para a célula FillForegnd pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |FillForegnd  <br/> |
   
Para obter uma referência para a célula FillForegnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowFill** <br/> |
|Índice da célula:  <br/> |**visFillForegnd** <br/> |
   

