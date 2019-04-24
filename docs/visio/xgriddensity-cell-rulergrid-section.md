---
title: Célula XGridDensity (seção &amp; Ruler Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Especifica o tipo de grade horizontal a ser utilizada.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328975"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Célula XGridDensity (seção &amp; Ruler Grid)

Especifica o tipo de grade horizontal a ser utilizada.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|,0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|duas  <br/> |Grande  <br/> |**visGridCoarse** <br/> |
|quatro  <br/> |Normal (padrão)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Funciona  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Comentários

Esta célula corresponde à opção horizontal **espaçamento da grade** na caixa de diálogo **grade da &amp; régua** (na guia **Exibir** , clique na seta **Mostrar** ). 
  
Para obter uma referência para a célula XGridDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |XGridDensity  <br/> |
   
Para obter uma referência para a célula XGridDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowRulerGrid** <br/> |
|Índice da célula:  <br/> |**visXGridDensity** <br/> |
   

