---
title: Célula FlyoutChild (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Determina se a linha é um menu de submenu filho da última linha acima da que não é filha de submenu.
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420861"
---
# <a name="flyoutchild-cell-actions-section"></a>Célula FlyoutChild (Seção Actions)

Determina se a linha é um menu de submenu filho da última linha acima da que não é filha de submenu. 
  
## <a name="remarks"></a>Comentários

Para obter uma referência à célula FlyoutChild pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome*  . Ações flyoutChildwhere.  *nome*  é o nome da linha Actions  <br/> |
   
Para obter uma referência à célula FlyoutChild pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice de linha:  <br/> |**visRowAction**  +   *i* onde *i* = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visActionFlyoutChild** <br/> |
   

