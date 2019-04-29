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
ms.openlocfilehash: be7ec4cccd53cc9d74811e2e45122c8bc29497d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438138"
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
| Índice de linha:  <br/> |**visRowPage** <br/> |
| Índice de célula:  <br/> |**visPageShdwOffsetY** <br/> |
   

