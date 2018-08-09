---
title: Célula PreviewScope (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Determina se o desenho conterá uma visualização. Se o seu desenho contiver uma visualização, ela determinará se irá exibir somente a primeira página ou todas as páginas do desenho.
ms.openlocfilehash: 865da052f710481c146d3c2692ddf506018be789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772590"
---
# <a name="previewscope-cell-document-properties-section"></a>Célula PreviewScope (Seção Document Properties)

Determina se o desenho conterá uma visualização. Se o seu desenho contiver uma visualização, ela determinará se irá exibir somente a primeira página ou todas as páginas do desenho.
  
|**Valor**|**Escopo de visualização**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Primeira página  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1  <br/> | Nenhum  <br/> |**visDocPreviewScopeNone** <br/> |
| 2  <br/> | Todas as páginas  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir esse valor na guia **Resumo** na caixa de diálogo **Propriedades** (clique no botão **Office** , clique na guia **informações** , clique em **Propriedades do documento**e, em seguida, clique em **Propriedades avançadas**).
  
Para obter uma referência para a célula PreviewScope pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PreviewScope  <br/> |
   
Para obter uma referência para a célula PreviewScope pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowDoc** <br/> |
| Índice da célula:  <br/> |**visDocPreviewScope** <br/> |
   

