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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434267"
---
# <a name="pagewidth-cell-page-properties-section"></a>Célula PageWidth (Seção Page Properties)

Determina a largura da página impressa em unidades de desenho.
  
## <a name="remarks"></a>Comentários

Você também pode definir a largura da  página na guia Tamanho da Página  da caixa de diálogo Configurar Página (na guia **Design,** clique na seta Configurar Página) ou reizing manualmente a página com o mouse.  Para fazer isso, mantenha pressionada a tecla CTRL e arraste a borda da página. 
  
Para obter uma referência para a célula PageWidth pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PageWidth  <br/> |
   
Para obter uma referência para a célula PageWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPage** <br/> |
|Índice de célula:  <br/> |**visPageWidth** <br/> |
   

