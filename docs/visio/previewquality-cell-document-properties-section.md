---
title: Célula PreviewQuality (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Determina se a visualização do desenho é um rascunho ou detalhada.
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772576"
---
# <a name="previewquality-cell-document-properties-section"></a>Célula PreviewQuality (Seção Document Properties)

Determina se a visualização do desenho é um rascunho ou detalhada.
  
|**Valor**|**Qualidade de visualização**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Rascunho  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Detalhada  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir esse valor na guia **Resumo** na caixa de diálogo **Propriedades** (clique no botão **Office** , clique na guia **informações** , clique em **Propriedades do documento**e, em seguida, clique em **Propriedades avançadas**).
  
Para obter uma referência para a célula PreviewQuality pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PreviewQuality  <br/> |
   
Para obter uma referência para a célula PreviewQuality pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowDoc** <br/> |
| Índice da célula:  <br/> |**visDocPreviewQuality** <br/> |
   

