---
title: Célula HideForApply (Seção Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Determina onde um estilo é mostrado na interface do usuário do Microsoft Visio.
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772033"
---
# <a name="hideforapply-cell-style-properties-section"></a>Célula HideForApply (Seção Style Properties)

Determina onde um estilo é mostrado na interface do usuário do Microsoft Visio.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | 
          O estilo é mostrado somente no **Gerenciador de Desenho**.
  <br/> |
| FALSO  <br/> | 
          O estilo é mostrado no **Gerenciador de Desenho**.
  <br/> |
   
## <a name="remarks"></a>Comentários

Quando um novo estilo tem por base um estilo oculto, o novo estilo não herda esse atributo.
  
Para fazer referência à célula HideForApply pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | HideForApply  <br/> |
   
Para fazer referência à célula HideForApply pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowStyle** <br/> |
| Índice da célula:  <br/> |**visStyleHidden** <br/> |
   

