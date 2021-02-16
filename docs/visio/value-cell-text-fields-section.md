---
title: Célula Value (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Contém a função para um campo.
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430942"
---
# <a name="value-cell-text-fields-section"></a>Célula Value (Seção Text Fields)

Contém a função para um campo.
  
## <a name="remarks"></a>Comentários

Você pode definir o valor desta célula usando a caixa de diálogo **Campo** (na guia **Inserir**, do grupo **Texto**, clique em **Campo**).
  
Para fazer referência à célula Value pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Para fazer referência à célula Value pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionTextField** <br/> |
|Índice de linha:  <br/> |**visRowField**  +   *i* onde *i* = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visFieldCell** <br/> |
   

