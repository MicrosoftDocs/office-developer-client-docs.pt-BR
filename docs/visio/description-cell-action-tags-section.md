---
title: Célula Description (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contém uma cadeia de caracteres que descreve a marca de ação, exibida como dica de ferramenta, quando os usuários posicionam o ponteiro sobre a marca.
ms.openlocfilehash: 3c365d24170f912624a2abdeeadd75140bea9a85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771715"
---
# <a name="description-cell-action-tags-section"></a>Célula Description (Seção Action Tags)

Contém uma cadeia de caracteres que descreve a marca de ação, exibida como dica de ferramenta, quando os usuários posicionam o ponteiro sobre a marca.
  
## <a name="remarks"></a>Comentários

Para fazer referência à célula Description pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Marcas inteligentes.  *nome* . Descrição onde SmartTags. *nome* é o nome da linha de marca de ação  <br/> |
   
Para fazer referência à célula Description pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice da linha:  <br/> |**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSmartTagDescription** <br/> |
   

