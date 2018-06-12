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
description: Y-deslocamento do botão de marca de ação em relação ao ponto definido pelas células X e Y.
ms.openlocfilehash: 8f8323d1f392654bf118ece2f78890f2a1b860ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773334"
---
# <a name="y-justify-cell-action-tags-section"></a>Célula Y Justify (Seção Action Tags)

*Y* -deslocamento do botão de marca de ação em relação ao ponto definido pelas células X e Y. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Justificado no topo (padrão).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | Centralizado.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | Justificado na base.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Coment�rios

As células X Justify e Y Justify determinam onde o botão de marca de ação é colocado em relação ao ponto definido nas células X e Y.
  
Para obter uma referência à célula Y Justify pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Marcas inteligentes.  *nome* . YJustify onde SmartTags. *nome* é o nome da linha de marca de ação  <br/> |
   
Para obter uma referência à célula Y Justify pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice da linha:  <br/> |**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSmartTagYJustify** <br/> |
   

