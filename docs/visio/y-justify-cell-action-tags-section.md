---
title: Célula Y Justify (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: O deslocamento y do botão de marca de ação em relação ao ponto definido pelas células X e Y.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357012"
---
# <a name="y-justify-cell-action-tags-section"></a>Célula Y Justify (Seção Action Tags)

O deslocamento *y* do botão de marca de ação em relação ao ponto definido pelas células X e y. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Justificado no topo (padrão).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | Centralizado.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| duas  <br/> | Justificado na base.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Comentários

As células X Justify e Y Justify determinam onde o botão de marca de ação é colocado em relação ao ponto definido nas células X e Y.
  
Para fazer referência à célula Y Justify pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SmartTags.  *nome* . YJustify onde SmartTags. *name*  é o nome da linha da marca de ação  <br/> |
   
Para fazer referência à célula X Justify pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice de linha:  <br/> |**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSmartTagYJustify** <br/> |
   

