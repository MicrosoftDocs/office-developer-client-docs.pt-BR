---
title: Célula XRulerDensity (seção &amp; Ruler Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Especifica as subdivisões horizontais da régua na página.
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411467"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Célula XRulerDensity (seção &amp; Ruler Grid)

Especifica as subdivisões horizontais da régua na página.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|,0  <br/> |Fixed  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Grande  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (padrão)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Funciona  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Comentários

Esta célula corresponde à opção horizontal **subdivisões** da caixa de diálogo **grade da &amp; régua** (na guia **Exibir** , clique na seta **Mostrar** ). 
  
Para obter uma referência para a célula XRulerDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |XRulerDensity  <br/> |
   
Para obter uma referência para a célula XRulerDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowRulerGrid** <br/> |
|Índice da célula:  <br/> |**visXRulerDensity** <br/> |
   

