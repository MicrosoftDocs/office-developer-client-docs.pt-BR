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
description: Determina a escala de desenho selecionada na caixa de diálogo Configurar Página (clique na seta Configurar Página na guia Início).
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428736"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>Célula DrawingScaleType (Seção Propriedades da página)

Determina a escala de desenho selecionada na caixa de diálogo **Configurar Página** (clique na seta **Configurar Página** na guia **Início**). 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Sem escala  <br/> |**visNoScale** <br/> |
| 1   <br/> | Escala arquitetônica  <br/> |**visArchitectural** <br/> |
| 2   <br/> | Escala de engenharia civil  <br/> |**visEngineering** <br/> |
| 3   <br/> | Escala personalizada  <br/> |**visScaleCustom** <br/> |
| 4   <br/> | Indicador  <br/> |**visScaleMetric** <br/> |
| 5   <br/> | Escala de engenharia mecânica  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula DrawingScaleType pelo nome de outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DrawingScaleType  <br/> |
   
Para obter uma referência à célula DrawingScaleType pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPage** <br/> |
| Índice de célula:  <br/> |**visPageDrawScaleType** <br/> |
   

