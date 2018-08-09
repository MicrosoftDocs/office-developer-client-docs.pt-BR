---
title: Célula Invisible (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Indica se uma ação é visível em um menu de atalho ou marca de ação.
ms.openlocfilehash: 8749b7d6db4a932b97c68ab5cf30b879a57d28f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772085"
---
# <a name="invisible-cell-actions-section"></a>Célula Invisible (Seção Actions)

Indica se uma ação é visível em um menu de atalho ou marca de ação. 
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A ação não é visível no menu.  <br/> |
|FALSO  <br/> |A ação é visível no menu (padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula Invisible pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome* . Ações de Invisiblewhere.  *nome* é o nome da linha Actions  <br/> |
   
Para obter uma referência para a célula Invisible pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice da linha:  <br/> |**visRowAction** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visActionInvisible** <br/> |
   

