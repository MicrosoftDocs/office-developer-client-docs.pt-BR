---
title: Célula noProofing (seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina se a ortografia é automaticamente corrigida e se os erros de ortografia são exibidos para a forma selecionada. Obtém um valor booliano.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357222"
---
# <a name="noproofing-cell-miscellaneous-section"></a>Célula noProofing (seção Miscellaneous)

Determina se a ortografia é automaticamente corrigida e se os erros de ortografia são exibidos para a forma selecionada. Obtém um **** valor booliano. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |A ortografia não é automaticamente corrigida e os erros de ortografia não são exibidos para a forma selecionada.  <br/> |
|FALSE  <br/> |A ortografia é automaticamente corrigida e os erros de ortografia são exibidos para a forma selecionada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula noProofing pelo nome, a partir de outra fórmula ou programa, usando a **** propriedade Cells, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |NoProofing  <br/> |
   
Para fazer referência à célula noProofing pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowMisc** <br/> |
|Índice da célula:  <br/> |**visObjNoProofing** <br/> |
   

