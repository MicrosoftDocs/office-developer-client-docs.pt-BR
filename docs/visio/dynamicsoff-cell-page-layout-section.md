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
ms.openlocfilehash: 72d65860d1a2ee37efd5287ae3f4baf54bd3addb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771780"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>Célula DynamicsOff (Seção Page Layout)

Determina se as formas de colocação serão movidas e se os conectores serão redirecionados em torno de outras formas e outros conectores na página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Desativar dinâmica.  <br/> |
| FALSO  <br/> | Ativar dinâmica.  <br/> |
   
## <a name="remarks"></a>Comentários

É possível desativar a dinâmica para aumentar o desempenho de sua solução. Por exemplo, se a sua solução adiciona formas de colocação a um desenho e você não quer que o aplicativo redirecione os conectores e reposicione as formas sempre que uma forma for adicionada, desative a dinâmica. Depois que a solução adicionar as formas, ative a dinâmica novamente.
  
Para obter uma referência à célula DynamicsOff pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | DynamicsOff  <br/> |
   
Para obter uma referência à célula DynamicsOff pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLODynamicsOff** <br/> |
   

