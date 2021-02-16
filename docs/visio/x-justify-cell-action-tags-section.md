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
description: O deslocamento x do botão de marca de ação em relação ao ponto definido pelas células X e Y.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414120"
---
# <a name="x-justify-cell-action-tags-section"></a>Célula X Justify (Seção Action Tags)

O  *deslocamento x*  do botão de marca de ação em relação ao ponto definido pelas células X e Y. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Justificado à esquerda (padrão).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1   <br/> | Centralizado.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2   <br/> | Justificado à direita.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Comentários

As células X Justify e Y Justify determinam onde o botão de marca de ação é colocado em relação ao ponto definido nas células X e Y. 
  
Para fazer referência à célula X Justify pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SmartTags.  *nome*  . XJustify onde SmartTags. *nome*  é o nome da linha da marca de ação  <br/> |
   
Para fazer referência à célula X Justify pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice de linha:  <br/> |**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visSmartTagXJustify** <br/> |
   

