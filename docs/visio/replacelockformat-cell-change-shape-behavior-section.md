---
title: Célula ReplaceLockFormat (seção de comportamento de forma alterar)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma. Se a célula ReplaceLockFormat de uma forma mestra é definida como verdadeiro (1), os valores de formatação do mestre substituir todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772694"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>Célula ReplaceLockFormat (seção de comportamento de forma alterar)

Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma. Se a célula **ReplaceLockFormat** de uma forma mestra é definida como verdadeiro (1), os valores de formatação do mestre substituir todos os valores correspondentes de uma forma que está sendo substituído pelo mestre. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Se a célula **ReplaceLockFormat** de uma forma mestra for definida como TRUE, os valores de formatação do mestre substituir todos os valores correspondentes de uma forma que está sendo substituído pelo mestre.  <br/> |
|FALSO  <br/> |Se a célula **ReplaceLockFormat** de uma forma mestra for definida como FALSE, a forma de substituição contém os valores de formatação locais da forma antigo após a operação de substituição.  <br/> |
   
## <a name="remarks"></a>Coment�rios

A célula **ReplaceLockFormat** determina se a forma mestra substitui os valores de formatação locais das células nas seções a seguir durante uma operação de substituição de forma: 
  
- Seção **Fill Format** 
    
- Seção **Line Format** 
    
- Seção de **Estilos Rápidos** 
    
- Seção de **Propriedades do tema** 
    
- Seção **Propriedades de gradiente** 
    
- Seção **Propriedades de bisel** 
    
- Seção de **Propriedades de efeito adicionais** 
    
- Seção de **Paradas de gradiente de linha** 
    
- Seção de **Paradas de gradiente de preenchimento** 
    
Para fazer referência à célula **ReplaceLockFormat** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ReplaceLockFormat  <br/> |
   
Para obter uma referência à célula **ReplaceLockFormat** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice da célula:  <br/> |**visReplaceLockFormat** <br/> |
   

