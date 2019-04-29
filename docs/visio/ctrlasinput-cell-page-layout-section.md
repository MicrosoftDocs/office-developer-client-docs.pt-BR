---
title: Célula CtrlAsInput (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Determina a forma pai ao utilizar formas com alças de controle. Esta célula determina o comportamento de todas as formas na página de desenho.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422618"
---
# <a name="ctrlasinput-cell-page-layout-section"></a>Célula CtrlAsInput (Seção Page Layout)

Determina a forma pai ao utilizar formas com alças de controle. Esta célula determina o comportamento de todas as formas na página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Define como pai a forma à qual a alça de controle está conectada.  <br/> |
| FALSE  <br/> | O padrão. Define como pai a forma que contém a alça de controle.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula CtrlAsInput pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | CtrlAsInput  <br/> |
   
Para fazer referência à célula CtrlAsInput pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLOCtrlAsInput** <br/> |
   

