---
title: Célula ConFixedCode (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Determina quando um conector é redirecionado.
ms.openlocfilehash: b2b9cde309c720493f0e46962b2fe6c2e79545d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404180"
---
# <a name="confixedcode-cell-shape-layout-section"></a>Célula ConFixedCode (Seção Shape Layout)

Determina quando um conector é redirecionado.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Redirecionar livremente  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1   <br/> |Redirecionar conforme necessário (redirecionamento manual)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2   <br/> |Nunca redirecionar  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3   <br/> |Redirecionar ao cruzar  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4   <br/> |Apenas para uso interno  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5   <br/> |Apenas para uso interno  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6   <br/> |Apenas para uso interno  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o valor desta célula selecionando um conector dinâmico, clicando em **Comportamento**, no grupo **Design da Forma**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **Conector**. 
  
Para obter uma referência para a célula ConFixedCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ConFixedCode  <br/> |
   
Para obter uma referência para a célula ConFixedCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice de célula:  <br/> |**visSLOConFixedCode** <br/> |
   

