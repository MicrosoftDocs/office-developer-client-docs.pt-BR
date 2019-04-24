---
title: Célula DynamicsOff (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Determina se as formas de colocação serão movidas e se os conectores serão redirecionados em torno de outras formas e outros conectores na página de desenho.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315715"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>Célula DynamicsOff (Seção Page Layout)

Determina se as formas de colocação serão movidas e se os conectores serão redirecionados em torno de outras formas e outros conectores na página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| TRUE  <br/> | Desativar dinâmica.  <br/> |
| FALSE  <br/> | Ativar dinâmica.  <br/> |
   
## <a name="remarks"></a>Comentários

É possível desativar a dinâmica para aumentar o desempenho de sua solução. Por exemplo, se a sua solução adiciona formas de colocação a um desenho e você não quer que o aplicativo redirecione os conectores e reposicione as formas sempre que uma forma for adicionada, desative a dinâmica. Depois que a solução adicionar as formas, ative a dinâmica novamente.
  
Para fazer referência à célula DynamicsOff pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DynamicsOff  <br/> |
   
Para fazer referência à célula DynamicsOff pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLODynamicsOff** <br/> |
   

