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
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327367"
---
# <a name="pagewidth-cell-page-properties-section"></a>Célula PageWidth (Seção Page Properties)

Determina a largura da página impressa em unidades de desenho.
  
## <a name="remarks"></a>Comentários

Você também pode definir a largura da página na **guia Tamanho da página** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** ) ou redimensionando manualmente a página com o mouse. Para fazer isso, mantenha pressionada a tecla CTRL e arraste a borda da página. 
  
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
   

