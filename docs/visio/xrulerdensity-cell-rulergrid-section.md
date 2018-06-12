---
title: Célula XRulerDensity (seção Ruler &amp; seção grade)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Especifica as subdivisões horizontais da régua na página.
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773305"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Célula XRulerDensity (seção Ruler &amp; seção grade)

Especifica as subdivisões horizontais da régua na página.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Fixa  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Grande  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (padrão)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Pequena  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Coment�rios

Essa célula corresponde à opção horizontal **Subdivisões** no **régua &amp; grade** caixa de diálogo (na guia **Exibir** , clique na seta **Mostrar** ). 
  
Para obter uma referência para a célula XRulerDensity pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |XRulerDensity  <br/> |
   
Para obter uma referência para a célula XRulerDensity pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowRulerGrid** <br/> |
|Índice da célula:  <br/> |**visXRulerDensity** <br/> |
   

