---
title: Célula NoProofing (seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina a ortografia foi corrigida automaticamente e se os erros de ortografia são exibidos para a forma selecionada. Recebe um valor booleano.
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19772416"
---
# <a name="noproofing-cell-miscellaneous-section"></a>Célula NoProofing (seção Miscellaneous)

Determina a ortografia foi corrigida automaticamente e se os erros de ortografia são exibidos para a forma selecionada. Recebe um valor **booleano** . 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Ortografia automaticamente não for corrigida e erros de ortografia não são exibidos para a forma selecionada.  <br/> |
|FALSO  <br/> |Corrigidas automaticamente de ortografia e erros de ortografia são exibidos para a forma selecionada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência à célula NoProofing pelo nome, a partir de outra fórmula ou de um programa, usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |NoProofing  <br/> |
   
Para obter uma referência à célula NoProofing pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowMisc** <br/> |
|Índice da célula:  <br/> |**visObjNoProofing** <br/> |
   

