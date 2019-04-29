---
title: Célula TextBkgndTrans (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Determina o nível de transparência para a cor do plano de fundo do bloco de texto da forma.
ms.openlocfilehash: f4c4dc7700c553bd4c9bee337220e357c4c5538a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408688"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a>Célula TextBkgndTrans (Seção Text Block Format)

Determina o nível de transparência para a cor do plano de fundo do bloco de texto da forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0 - 100  <br/> |Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com um plano de fundo de texto completamente transparente tenha a mesma aparência de uma forma sem plano de fundo de texto na página de desenho, ela interage com os outros objetos da página da mesma forma que se a transparência fosse 0%.
  
Você pode também definir o valor utilizando o controle deslizante na guia **Fonte** da caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**). 
  
Para obter uma referência para a célula TextBkgndTrans pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |TextBkgndTrans  <br/> |
   
Para obter uma referência para a célula TextBkgndTrans pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowText** <br/> |
|Índice da célula:  <br/> |**visTxtBlkBkgndTrans** <br/> |
   

