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
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356032"
---
# <a name="previewquality-cell-document-properties-section"></a>Célula PreviewQuality (Seção Document Properties)

Determina se a visualização do desenho é um rascunho ou detalhada.
  
|**Valor**|**Qualidade de visualização**|**Constante de automação**|
|:-----|:-----|:-----|
| ,0  <br/> | Rascunho  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Análise  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir esse valor na guia **Resumo** da caixa de diálogo **Propriedades** (clique no botão **Office** , clique na guia **informações** , em **Propriedades do documento**e em **Propriedades avançadas**).
  
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
   

