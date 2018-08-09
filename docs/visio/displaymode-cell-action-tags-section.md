---
title: Célula DisplayMode (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Determina se a marca de ação aparece quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771711"
---
# <a name="displaymode-cell-action-tags-section"></a>Célula DisplayMode (Seção Action Tags)

Determina se a marca de ação aparece quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Modo de exibição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Aparece quando o mouse é pausado sobre a marca (padrão).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | Exibido enquanto a forma é selecionada.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | Sempre exibido.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Comentários

As marcas de ação não aparecem no material impresso nem publicado. 
  
Se uma marca de ação for definida para uma página e essa célula contiver o valor 1, a marca nunca será exibida pois a página não pode ser selecionada. 
  
Para fazer referência à célula DisplayMode pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Marcas inteligentes.  *nome* . DisplayMode onde SmartTags. *nome* é o nome da linha de marca de ação  <br/> |
   
Para obter uma referência para a célula DisplayMode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice da linha:  <br/> |**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSmartTagDisplayMode** <br/> |
   

