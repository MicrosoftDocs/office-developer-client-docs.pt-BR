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
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332393"
---
# <a name="tagname-cell-action-tags-section"></a>Célula TagName (Seção Action Tags)

Nome da marca de ação usada como chave para associar a marca de ação a suas ações.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

 A célula TagName na seção Action Tags trabalha junto com a célula TagName na seção Actions para associar a marca de ação a suas ações. As linhas na seção Actions também têm uma célula TagName e essas linhas com o mesmo valor da célula TagName que esta célula definem as ações a serem tomadas para esta marca de ação. 
  
Para fazer referência à célula TagName pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SmartTags.  *nome* . TagName onde SmartTags. *name*  é o nome da linha da marca de ação  <br/> |
   
Para fazer referência à célula TagName pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice de linha:  <br/> |**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSmartTagName** <br/> |
   

