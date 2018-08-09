---
title: Célula ShdwOffsetY (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada verticalmente da forma.
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772965"
---
# <a name="shdwoffsety-cell-page-properties-section"></a>Célula ShdwOffsetY (Seção Page Properties)

Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada verticalmente da forma.
  
## <a name="remarks"></a>Comentários

Esse valor é definido na caixa de diálogo **Configurar página** (na guia **Design**, clique na seta **Configurar Página**). Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o deslocamento da sombra será o mesmo. 
  
Para obter uma referência para a célula ShdwOffsetY pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwOffsetY  <br/> |
   
Para obter uma referência para a célula ShdwOffsetY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageShdwOffsetY** <br/> |
   

