---
title: Célula PageShapeSplit (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Indica se as formas na página podem ser divididas automaticamente.
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422016"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>Célula PageShapeSplit (Seção Page Layout)

Indica se as formas na página podem ser divididas automaticamente.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|,0  <br/> |Não permite divisão automática de forma.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Permite divisão automática de forma (padrão).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Comentários

A divisão automática de formas é habilitada ou desabilitada em três níveis diferentes: aplicativo, página e forma. Por padrão, a divisão é habilitada no aplicativo e na página. A configuração padrão para formas varia por tipo de desenho. 
  
Para habilitar ou desabilitar a divisão no nível do aplicativo, use a **configuração Habilitar divisão de conector** na guia **avançado** da caixa de diálogo **Opções do Visio** (clique no botão **Office** , em **Opções** no **Visio** e, em seguida, clique em **avançado** . 
  
Para habilitar ou desabilitar a divisão no nível da forma, consulte as células ShapeSplit e ShapeSplittable. 
  
Para obter uma referência para a célula PageShapeSplit pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PageShapeSplit  <br/> |
   
Para obter uma referência para a célula PageShapeSplit pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLOSplit** <br/> |
   

