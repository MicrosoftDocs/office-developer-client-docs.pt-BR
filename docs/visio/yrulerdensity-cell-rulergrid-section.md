---
title: Célula YRulerDensity (Seção Ruler &amp; Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Especifica as subdivisões verticais da régua na página.
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773337"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Célula YRulerDensity (Seção Ruler &amp; Grid)

Especifica as subdivisões verticais da régua na página.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Fixa  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Grande  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (padrão)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Pequena  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Comentários

Essa célula corresponde à opção vertical **Subdivisões** no **régua &amp; grade** caixa de diálogo (na guia **Exibir** , clique na seta **Mostrar** ). 
  
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
   

