---
title: Célula DoubleULine (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Determina se o intervalo de texto contém um sublinhado duplo abaixo dele.
ms.openlocfilehash: d0a07d8c86bd7e9ed3eb14074dda164f82c92475
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771769"
---
# <a name="doubleuline-cell-character-section"></a>Célula DoubleULine (Seção Character)

Determina se o intervalo de texto contém um sublinhado duplo abaixo dele.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O texto contém sublinhado duplo abaixo dele.  <br/> |
|FALSO  <br/> |O texto não contém sublinhado duplo abaixo dele.  <br/> |
   
## <a name="remarks"></a>Comentários

A célula DoubleULine conterá informações de formatação aplicada a um subintervalo do texto de uma forma se a seção Caractere contiver diversas linhas. Caso contrário, ela conterá informações de formatação para todo o texto da forma.
  
Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (clique na seta **Fonte** na guia **Página Inicial**). 
  
Para obter uma referência para a célula DoubleULine pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char.DblUnderline [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência para a célula DoubleULine pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterDblUnderline** <br/> |
   

