---
title: Célula ShdwForegnd (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Determina a cor utilizada para o primeiro plano (traço) do padrão de preenchimento de sombra projetada da forma.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422247"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>Célula ShdwForegnd (Seção Fill Format)

Determina a cor utilizada para o primeiro plano (traço) do padrão de preenchimento de sombra projetada da forma.
  
## <a name="remarks"></a>Comentários

Para definir a cor, insira um número de 0 a 23, que serve como um índice para uma coleção de cores.
  
Para inserir uma cor personalizada, utilize a função RGB ou HSL. O valor de uma cor personalizada é sua cor RGB, e RGB( *r, g, b*), em vez de um número, será mostrado na janela ShapeSheet. Quando utilizadas em operações numéricas, as cores têm valores iguais e superiores a 24. 
  
É possível definir a transparência da cor do primeiro plano do padrão de preenchimento da sombra projetada da forma na célula ShdwForegndTrans.
  
Para obter uma referência para a célula ShdwForegnd pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwForegnd  <br/> |
   
Para obter uma referência para a célula ShdwForegnd pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowFill** <br/> |
| Índice de célula:  <br/> |**visFillShdwForegnd** <br/> |
   

