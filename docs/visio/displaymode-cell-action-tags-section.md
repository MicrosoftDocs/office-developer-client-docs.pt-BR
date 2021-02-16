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
description: Determina se a marca de ação é exibida quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415814"
---
# <a name="displaymode-cell-action-tags-section"></a>Célula DisplayMode (Seção Action Tags)

Determina se a marca de ação é exibida quando o usuário move o ponteiro sobre a marca, quando a forma é selecionada ou sempre.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Modo de Exibição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Aparece quando o mouse é pausado sobre a marca (o padrão).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1   <br/> | Exibido enquanto a forma é selecionada.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2   <br/> | Sempre exibido.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Comentários

As marcas de ação não aparecem no material impresso nem publicado. 
  
Se uma marca de ação for definida para uma página e essa célula contiver o valor 1, a marca nunca será exibida pois a página não pode ser selecionada. 
  
Para fazer referência à célula DisplayMode pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SmartTags.  *nome*  . DisplayMode onde SmartTags. *nome*  é o nome da linha da marca de ação  <br/> |
   
Para fazer referência à célula DisplayMode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice de linha:  <br/> |**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visSmartTagDisplayMode** <br/> |
   

