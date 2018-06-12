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
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772954"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>Célula ShdwForegnd (Seção Fill Format)

Determina a cor utilizada para o primeiro plano (traço) do padrão de preenchimento de sombra projetada da forma.
  
## <a name="remarks"></a>Comentários

Para definir a cor, insira um número de 0 a 23, que serve como um índice para uma coleção de cores.
  
Para inserir uma cor personalizada, use a função RGB ou HSL. O valor de uma cor personalizada é a cor RGB e RGB ( *r, g, b*), em vez de um número, será exibido na janela ShapeSheet. Quando usado em operações numéricas, as cores têm valores de 24 e acima. 
  
É possível definir a transparência da cor do primeiro plano do padrão de preenchimento da sombra projetada da forma na célula ShdwForegndTrans.
  
Para obter uma referência para a célula ShdwForegnd pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwForegnd  <br/> |
   
Para obter uma referência para a célula ShdwForegnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowFill** <br/> |
| Índice da célula:  <br/> |**visFillShdwForegnd** <br/> |
   

