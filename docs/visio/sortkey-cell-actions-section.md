---
title: Célula SortKey (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Um número que determina a ordem das ações que aparecem no menu de marca de ação ou atalho.
ms.openlocfilehash: d4eb98055f199f603003b068dca9fa7b4e377e52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419657"
---
# <a name="sortkey-cell-actions-section"></a>Célula SortKey (Seção Actions)

Um número que determina a ordem de ações exibidas em um menu de atalho ou de marca de ação.
  
> [!NOTE]
> Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes. 
  
## <a name="remarks"></a>Comentários

As ações em um menu de atalho ou de marca de ação são exibidas no menu, classificadas do valor mais baixo para o mais alto, com a numeração mais baixa exibida na parte superior do menu. Se duas linhas de ação tiverem o mesmo valor de célula SortKey, a ordem será determinada pela ordem física da linha. O padrão é 0 (zero).
  
Para obter uma referência para a célula SortKey pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Ações. *nome*  . Ações sortKeywhere.  *nome*  é o nome da linha Actions  <br/> |
   
Para obter uma referência para a célula SortKey pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionAction** <br/> |
|Índice de linha:  <br/> |**visRowAction**  +   *i* onde *i* = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visActionSortKey** <br/> |
   

