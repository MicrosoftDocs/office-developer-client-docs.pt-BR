---
title: Célula YGridDensity (Seção Ruler &amp; Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Especifica o tipo de grade vertical a ser utilizada.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429807"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Célula YGridDensity (Seção Ruler &amp; Grid)

Especifica o tipo de grade vertical a ser utilizada.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|2   <br/> |Insupernte  <br/> |**visGridCoarse** <br/> |
|4   <br/> |Normal (padrão)  <br/> |**visGridNormal** <br/> |
|8   <br/> |Bem  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Comentários

Essa célula corresponde à opção de espaçamento **vertical** Grid  na caixa de diálogo **Grade &amp;** de Régua (na guia Exibir, clique na **seta Mostrar).** 
  
Para obter uma referência para a célula YGridDensity pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |YGridDensity  <br/> |
   
Para obter uma referência para a célula YGridDensity pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowRulerGrid** <br/> |
|Índice de célula:  <br/> |**visYGridDensity** <br/> |
   

