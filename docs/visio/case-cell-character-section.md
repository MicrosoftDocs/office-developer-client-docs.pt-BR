---
title: Célula Case (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Determina a utilização de maiúsculas e minúsculas no texto de uma forma. Todas as letras maiúsculas (1) e maiúsculas iniciais (2) não alteram a aparência do texto digitado completamente em letras maiúsculas. O texto deve ser digitado em letras minúsculas para que essas opções possam ter efeito.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434344"
---
# <a name="case-cell-character-section"></a>Célula Case (Seção Character)

Determina a utilização de maiúsculas e minúsculas no texto de uma forma. Todas as letras maiúsculas (1) e maiúsculas iniciais (2) não alteram a aparência do texto digitado completamente em letras maiúsculas. O texto deve ser digitado em letras minúsculas para que essas opções possam ter efeito.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 0  <br/> | Maiúsculas e minúsculas normais  <br/> |**visCaseNormal** <br/> |
| 1   <br/> | Tudo em letras maiúsculas  <br/> |**visCaseAllCaps** <br/> |
| 2   <br/> | Somente as iniciais maiúsculas  <br/> |**visCaseInitialCaps** <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula Case pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Char.Case[  *i*  ] where  *i*  = <1>, 2, 3, ...  <br/> |
   
Para fazer referência à célula Case pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionCharacter** <br/> |
| Índice de linha:  <br/> |**visRowCharacter**  +   *i* onde *i* = 0, 1, 2, ...  <br/> |
| Índice da célula:  <br/> |**visCharacterCase** <br/> |
   

