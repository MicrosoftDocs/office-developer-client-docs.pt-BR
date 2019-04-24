---
title: Célula YRulerDensity (seção &amp; Ruler Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Especifica as subdivisões verticais da régua na página.
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357201"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Célula YRulerDensity (seção &amp; Ruler Grid)

Especifica as subdivisões verticais da régua na página.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|,0  <br/> |Fixed  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Grande  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (padrão)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Funciona  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Comentários

Esta célula corresponde à opção de **subdivisões** verticais da caixa de diálogo **grade &amp; da régua** (na guia **Exibir** , clique na seta **Mostrar** ). 
  
Para obter uma referência para a célula YRulerDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |YRulerDensity  <br/> |
   
Para obter uma referência para a célula YRulerDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowRulerGrid** <br/> |
|Índice da célula:  <br/> |**visYRulerDensity** <br/> |
   

