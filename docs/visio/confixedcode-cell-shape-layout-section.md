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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284459"
---
# <a name="confixedcode-cell-shape-layout-section"></a>Célula ConFixedCode (Seção Shape Layout)

Determina quando um conector é redirecionado.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|,0  <br/> |Redirecionar livremente  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |Redirecionar conforme necessário (redirecionamento manual)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|duas  <br/> |Nunca redirecionar  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3D  <br/> |Redirecionar ao cruzar  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|quatro  <br/> |Apenas para uso interno  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|0,5  <br/> |Apenas para uso interno  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6  <br/> |Apenas para uso interno  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula selecionando um conector dinâmico, clicando em **comportamento** no grupo **design da forma** na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **conector** . 
  
Para obter uma referência para a célula ConFixedCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ConFixedCode  <br/> |
   
Para obter uma referência para a célula ConFixedCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOConFixedCode** <br/> |
   

