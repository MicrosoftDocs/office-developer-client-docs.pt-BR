---
title: Célula TxtWidth (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Determina a largura do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: ecba66aaf1f7eeb6d16c6b0d4c6569aed051910f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773215"
---
# <a name="txtwidth-cell-text-transform-section"></a>Célula TxtWidth (Seção Text Transform)

Determina a largura do bloco de texto. A fórmula padrão é:
  
= A largura \* 1
  
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula TxtWidth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TxtWidth  <br/> |
   
Para obter uma referência à célula TxtWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowTextXForm** <br/> |
| Índice da célula:  <br/> |**visXFormWidth** <br/> |
   

