---
title: Célula NoCtlHandles (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: Alterna entre exibir ou não as alças de controle da forma selecionada.
ms.openlocfilehash: 897e4cd97eeab8797f2652285ba395603c41a8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772407"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a>Célula NoCtlHandles (Seção Miscellaneous)

Alterna entre exibir ou não as alças de controle da forma selecionada.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | As alças de controle não são exibidas ao selecionar uma forma.  <br/> |
| FALSO  <br/> | As alças de controle são exibidas ao selecionar uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula NoCtlHandles pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | NoCtlHandles  <br/> |
   
Para fazer referência à célula NoCtlHandles pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visNoCtlHandles** <br/> |
   

