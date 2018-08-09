---
title: Célula PageWidth (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Determina a largura da página impressa em unidades de desenho.
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772471"
---
# <a name="pagewidth-cell-page-properties-section"></a>Célula PageWidth (Seção Page Properties)

Determina a largura da página impressa em unidades de desenho.
  
## <a name="remarks"></a>Comentários

Você também pode definir a largura da página na guia **Tamanho da página** da caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ) ou redimensionar manualmente a página com o mouse. Para fazer isso, arraste a borda da página, mantendo pressionada a tecla CTRL. 
  
Para obter uma referência para a célula PageWidth pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PageWidth  <br/> |
   
Para obter uma referência para a célula PageWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPage** <br/> |
|Índice da célula:  <br/> |**visPageWidth** <br/> |
   

