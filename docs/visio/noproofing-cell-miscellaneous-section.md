---
title: Célula NoProofing (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina se a ortografia será corrigida automaticamente e se erros de ortografia serão exibidos para a forma selecionada. Aceita um valor Boolean.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431250"
---
# <a name="noproofing-cell-miscellaneous-section"></a>Célula NoProofing (Seção Miscellaneous)

Determina se a ortografia será corrigida automaticamente e se erros de ortografia serão exibidos para a forma selecionada. Aceita um **valor Boolean.** 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A ortografia não é corrigida automaticamente e os erros de ortografia não são exibidos para a forma selecionada.  <br/> |
|FALSE  <br/> |A ortografia é corrigida automaticamente e os erros de ortografia são exibidos para a forma selecionada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula NoProofing pelo nome, a partir de outra fórmula ou programa, usando a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |NoProofing  <br/> |
   
Para fazer referência à célula NoProofing pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowMisc** <br/> |
|Índice de célula:  <br/> |**visObjNoProofing** <br/> |
   

