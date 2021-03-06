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
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426503"
---
# <a name="previewscope-cell-document-properties-section"></a>Célula PreviewScope (Seção Document Properties)

Determina se o desenho conterá uma visualização. Se o seu desenho contiver uma visualização, ela determinará se irá exibir somente a primeira página ou todas as páginas do desenho.
  
|**Valor**|**Escopo de visualização**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Primeira página  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1   <br/> | Nenhum  <br/> |**visDocPreviewScopeNone** <br/> |
| 2   <br/> | Todas as páginas  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir  esse valor na guia Resumo da caixa de diálogo Propriedades (clique no botão **Office,** clique na guia Informações, em Propriedades do Documento e em **Propriedades Avançadas).**  
  
Para obter uma referência para a célula PreviewScope pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PreviewScope  <br/> |
   
Para obter uma referência para a célula PreviewScope pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowDoc** <br/> |
| Índice de célula:  <br/> |**visDocPreviewScope** <br/> |
   

