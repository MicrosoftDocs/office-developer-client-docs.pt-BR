---
title: Célula Transparency (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Determina o nível de transparência de um intervalo na cor de texto de uma forma.
ms.openlocfilehash: 8619ec25372ae163fff1759aca36ff6693820e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280980"
---
# <a name="transparency-cell-character-section"></a>Célula Transparency (Seção Character)

Determina o nível de transparência de um intervalo na cor de texto de uma forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0 - 100  <br/> |Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com texto completamente transparente tenha a mesma aparência de uma forma sem texto na página de desenho, ela interage com os outros objetos da página da mesma forma que se a transparência fosse 0%.
  
Você também pode definir esse valor usando o controle deslizante na guia **fonte** da caixa de diálogo **texto** (na guia **página inicial** , clique na seta **fonte** ). 
  
Se a seção Caracteres contiver diversas linhas, a célula Transparency conterá informações de formatação aplicada a um subintervalo de texto de uma forma. Caso contrário, ela conterá informações de formatação para todo o texto da forma.
  
Para obter uma referência para a célula Transparency pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Char. ColorTrans [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Transparency pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionCharacter** <br/> |
|Índice da linha:  <br/> |**visRowCharacter** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCharacterColorTrans** <br/> |
   

