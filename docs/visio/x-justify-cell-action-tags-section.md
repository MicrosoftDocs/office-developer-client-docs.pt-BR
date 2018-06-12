---
title: Célula X Justify (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: O - deslocamento x do botão de marca de ação em relação ao ponto definido pelas células X e Y.
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773304"
---
# <a name="x-justify-cell-action-tags-section"></a>Célula X Justify (Seção Action Tags)

*X* -deslocamento do botão de marca de ação em relação ao ponto definido pelas células X e Y. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Justificado à esquerda (padrão).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Centralizado.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | Justificado à direita.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Coment�rios

As células X Justify e Y Justify determinam onde o botão de marca de ação é colocado em relação ao ponto definido nas células X e Y. 
  
Para fazer referência à célula X Justify pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Marcas inteligentes.  *nome* . XJustify onde SmartTags. *nome* é o nome da linha de marca de ação  <br/> |
   
Para obter uma referência à célula X Justify pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice da linha:  <br/> |**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSmartTagXJustify** <br/> |
   

