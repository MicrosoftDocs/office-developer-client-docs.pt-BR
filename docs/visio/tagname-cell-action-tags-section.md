---
title: Célula TagName (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Nome da marca de ação usada como chave para associar a marca de ação a suas ações.
ms.openlocfilehash: dbac3d4dff9d2ffd18bba75db56cafc08f5e0ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773095"
---
# <a name="tagname-cell-action-tags-section"></a>Célula TagName (Seção Action Tags)

Nome da marca de ação usada como chave para associar a marca de ação a suas ações.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

 A célula TagName na seção Action Tags funciona em conjunto com a célula TagName na seção Actions para associar uma marca de ação a suas ações. Linhas na seção Actions também têm uma célula TagName e as linhas com o mesmo valor da célula TagName como essa célula definem ações a serem tomadas para esta marca de ação. 
  
Para obter uma referência à célula TagName pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Marcas inteligentes.  *nome* . TagName onde SmartTags. *nome* é o nome da linha de marca de ação  <br/> |
   
Para obter uma referência à célula TagName pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice da linha:  <br/> |**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSmartTagName** <br/> |
   

