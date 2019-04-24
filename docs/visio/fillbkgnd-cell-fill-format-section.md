---
title: Célula FillBkgnd (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Determina a cor utilizada para o plano de fundo (preenchimento) do padrão de preenchimento da forma.
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322509"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>Célula FillBkgnd (Seção Fill Format)

Determina a cor utilizada para o plano de fundo (preenchimento) do padrão de preenchimento da forma.
  
## <a name="remarks"></a>Comentários

Para definir a cor, insira um número de 0 a 23.
  
Para inserir uma cor personalizada, utilize a função RGB ou HSL. O valor de uma cor personalizada é a cor RGB, e é isso (*r, g, b*), e não um número, que será mostrado na janela ShapeSheet. Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24. 
  
É possível definir a transparência de preenchimento do plano de fundo na célula FillBkgndTrans. 
  
Para obter uma referência para a célula FillBkgnd pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | FillBkgnd  <br/> |
   
Para obter uma referência para a célula FillBkgnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowFill** <br/> |
| Índice da célula:  <br/> |**visFillBkgnd** <br/> |
   

