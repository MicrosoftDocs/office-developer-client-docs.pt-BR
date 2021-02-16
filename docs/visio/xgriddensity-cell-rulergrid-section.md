---
title: Célula XGridDensity (Seção Ruler &amp; Grid)
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436038"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Célula XGridDensity (Seção Ruler &amp; Grid)

Especifica o tipo de grade horizontal a ser utilizada.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|2   <br/> |Insupernte  <br/> |**visGridCoarse** <br/> |
|4   <br/> |Normal (padrão)  <br/> |**visGridNormal** <br/> |
|8   <br/> |Bem  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Comentários

Essa célula corresponde à opção de espaçamento **horizontal** Grid  na caixa de diálogo **Grade &amp;** de Régua (na guia Exibir, clique na **seta** Mostrar). 
  
Para obter uma referência para a célula XGridDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |XGridDensity  <br/> |
   
Para obter uma referência para a célula XGridDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowRulerGrid** <br/> |
|Índice de célula:  <br/> |**visXGridDensity** <br/> |
   

