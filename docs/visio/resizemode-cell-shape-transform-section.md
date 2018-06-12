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
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772753"
---
# <a name="resizemode-cell-shape-transform-section"></a>Célula ResizeMode (Seção Shape Transform)

Mostra a definição de comportamento de redimensionamento atual da forma.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Usar configuração do grupo.  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |Apenas reposicionar.  <br/> |**visXFormResizeSpread** <br/> |
|2  <br/> |Escala com grupo.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Coment�rios

Você também pode definir esse valor na guia **comportamento** , na caixa de diálogo **comportamento** (na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md), no grupo **Design da forma** , clique em **comportamento**). Para obter uma referência à célula ResizeMode pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ResizeMode  <br/> |
   
Para obter uma referência à célula ResizeMode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowXFormOut** <br/> |
|Índice da célula:  <br/> |**visXFormResizeMode** <br/> |
   

