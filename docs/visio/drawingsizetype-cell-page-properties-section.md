---
title: Célula DrawingSizeType (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm275
localization_priority: Normal
ms.assetid: 7fe270e8-0dff-bf1f-dfc0-c0608af79f59
description: Determina o tamanho do desenho.
ms.openlocfilehash: a87f37ac79d00aeb064072389db432421b33d2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771765"
---
# <a name="drawingsizetype-cell-page-properties-section"></a>Célula DrawingSizeType (Seção Page Properties)

Determina o tamanho do desenho.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Mesmo que a impressora  <br/> |**visPrintSetup** <br/> |
|1  <br/> |Ajustar página ao conteúdo do desenho  <br/> |**visTight** <br/> |
|2  <br/> |Padrão  <br/> |**visStandard** <br/> |
|3  <br/> |Tamanho da página personalizada  <br/> |**visCustom** <br/> |
|4  <br/> |Tamanho do desenho em escala personalizado  <br/> |**visLogical** <br/> |
|5  <br/> |Métrico (ISO)  <br/> |**visDSMetric** <br/> |
|6  <br/> |Engenharia ANSI  <br/> |**visDSEngr** <br/> |
|7  <br/> |Arquitetura ANSI  <br/> |**visDSArch** <br/> |
   
## <a name="remarks"></a>Comentários

Para definir o tamanho do desenho, use a caixa de diálogo **Configurar Página** (clique na seta **Configurar Página** na guia **Design**) ou redimensione manualmente a página com o mouse. 
  
Para obter uma referência para a célula DrawingSizeType pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |DrawingSizeType  <br/> |
   
Para obter uma referência para a célula DrawingSizeType pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPage** <br/> |
|Índice da célula:  <br/> |**visPageDrawSizeType** <br/> |
   

