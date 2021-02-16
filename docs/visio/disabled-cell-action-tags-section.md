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
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439664"
---
# <a name="disabled-cell-action-tags-section"></a>Célula Disabled (Seção Action Tags)

Indica se a marca de ação é exibida na janela de desenho.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | A marca de ação está desabilitada.  <br/> |
| FALSE  <br/> | A marca de ação está habilitada (padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Quando uma marca de ação está desabilitada, ela não é exibida até ser reabilitada. 
  
Para fazer referência à célula Disabled pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SmartTags.  *nome*  . Desabilitado onde SmartTags. *nome*  é o nome da linha da marca de ação  <br/> |
   
Para fazer referência à célula Disabled pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice de linha:  <br/> |**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visSmartTagDisabled** <br/> |
   

