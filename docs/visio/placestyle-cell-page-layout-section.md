---
title: Célula PlaceStyle (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Determina como as formas são posicionadas na página quando dispostas com o uso da caixa de diálogo Configurar Layout (na guia Design, no grupo Layout, clique em Refazer o Layout da Página e depois em Mais Opções de Layout).
ms.openlocfilehash: 251bee427c732fe782c85c4991df07a1deb2a4dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772491"
---
# <a name="placestyle-cell-page-layout-section"></a>Célula PlaceStyle (Seção Page Layout)

Determina como as formas são posicionadas na página quando dispostas com o uso da caixa de diálogo **Configurar Layout** (na guia **Design**, no grupo **Layout**, clique em **Refazer o Layout da Página** e depois em **Mais Opções de Layout**).
  
## <a name="remarks"></a>Comentários

Também é possível definir o valor dessa célula na caixa de diálogo **Configurar Layout**. 
  
Para obter uma referência à célula PlaceStyle pelo nome a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PlaceStyle  <br/> |
   
Para fazer referência à célula PlaceStyle pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLOPlaceStyle** <br/> |
   

