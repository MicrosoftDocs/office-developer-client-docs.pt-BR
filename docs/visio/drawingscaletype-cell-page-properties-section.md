---
title: Célula DrawingScaleType (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Determina a escala do desenho selecionada na caixa de diálogo Configurar Página (clique na seta Configurar Página na guia Página Inicial).
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771777"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>Célula DrawingScaleType (Seção Page Properties)

Determina a escala do desenho selecionada na caixa de diálogo **Configurar Página** (clique na seta **Configurar Página** na guia **Página Inicial**). 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Sem escala  <br/> |**visNoScale** <br/> |
| 1  <br/> | Escala arquitetônica  <br/> |**visArchitectural** <br/> |
| 2  <br/> | Escala de engenharia civil  <br/> |**visEngineering** <br/> |
| 3  <br/> | Escala personalizada  <br/> |**visScaleCustom** <br/> |
| 4  <br/> | Métrica  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | Escala de engenharia mecânica  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula DrawingScaleType pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DrawingScaleType  <br/> |
   
Para obter uma referência para a célula DrawingScaleType pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageDrawScaleType** <br/> |
   

