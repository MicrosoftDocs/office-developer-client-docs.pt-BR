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
ms.openlocfilehash: 448e721d8dd6e287c61488e28b875f76d0fa2977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771575"
---
# <a name="confixedcode-cell-shape-layout-section"></a>Célula ConFixedCode (Seção Shape Layout)

Determina quando um conector é redirecionado.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |
          Redirecionar livremente
  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |
          Redirecionar conforme necessário (redirecionamento manual)
  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |
          Nunca redirecionar
  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |
          Redirecionar ao cruzar
  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4  <br/> |Somente para uso interno  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5  <br/> |Somente para uso interno  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6  <br/> |Somente para uso interno  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Comentários

Você pode também definir o valor desta célula selecionando um conector dinâmico, clicando em **comportamento** , no grupo **Design** da forma na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, clicando na guia **conector** . 
  
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
   

