---
title: Célula NoLiveDynamics (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Determina se uma forma é redimensionada ou girada dinamicamente à medida que é manipulada.
ms.openlocfilehash: 043571243fe3698561bee8632e7fd18db04c9330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772412"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a>Célula NoLiveDynamics (Seção Miscellaneous)

Determina se uma forma é redimensionada ou girada dinamicamente à medida que é manipulada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Não atualizar dinamicamente a forma à medida que é manipulada.  <br/> |
| FALSO  <br/> | Atualizar dinamicamente a forma à medida que é manipulada.  <br/> |
   
## <a name="remarks"></a>Comentários

À medida que uma forma bidimensional (2D) é redimensionada ou girada sem a dinâmica ao vivo, é possível visualizar uma caixa de seleção. Se a forma for unidimensional (1D), o comentário visual terá como base o valor da célula DynFeedback.
  
Para fazer referência à célula NoLiveDynamics pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | NoLiveDynamics  <br/> |
   
Para fazer referência à célula NoLiveDynamics pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visNoLiveDynamics** <br/> |
   

