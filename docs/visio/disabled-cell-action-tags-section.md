---
title: Célula Disabled (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Indica se a marca de ação é exibida na janela de desenho.
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771718"
---
# <a name="disabled-cell-action-tags-section"></a>Célula Disabled (Seção Action Tags)

Indica se a marca de ação é exibida na janela de desenho.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A marca de ação está desabilitada.  <br/> |
| FALSO  <br/> | A marca de ação está habilitada (padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Quando uma marca de ação está desabilitada, ela não é exibida até ser reabilitada. 
  
Para fazer referência à célula Disabled pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Marcas inteligentes.  *nome* . Desabilitado onde SmartTags. *nome* é o nome da linha de marca de ação  <br/> |
   
Para obter uma referência para a célula Disabled pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice da linha:  <br/> |**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visSmartTagDisabled** <br/> |
   

