---
title: Célula ResizeMode (Seção Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Mostra a definição de comportamento de redimensionamento atual da forma.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421960"
---
# <a name="resizemode-cell-shape-transform-section"></a>Célula ResizeMode (Seção Shape Transform)

Mostra a definição de comportamento de redimensionamento atual da forma.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Usar configuração do grupo.  <br/> |**visXFormResizeDontCare** <br/> |
|1   <br/> |Apenas reposicionar.  <br/> |**visXFormResizeSpread** <br/> |
|2   <br/> |Escala com grupo.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir esse valor  na guia Comportamento [](run-in-developer-mode-display-the-developer-tab.md)na caixa de diálogo Comportamento (na guia Desenvolvedor, no grupo **Design** da Forma, clique em **Comportamento).**  Para obter uma referência à célula ResizeMode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ResizeMode  <br/> |
   
Para obter uma referência para a célula ResizeMode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowXFormOut** <br/> |
|Índice de célula:  <br/> |**visXFormResizeMode** <br/> |
   

