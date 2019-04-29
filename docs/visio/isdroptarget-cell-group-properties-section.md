---
title: Célula IsDropTarget (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Determina se a forma pode ser adicionada ao grupo sendo solta nele.
ms.openlocfilehash: 50f545b3cbd4f7e1541a7f5e8ca32c34d0429c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410788"
---
# <a name="isdroptarget-cell-group-properties-section"></a>Célula IsDropTarget (Seção Group Properties)

Determina se a forma pode ser adicionada ao grupo sendo solta nele.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A forma pode ser adicionada ao grupo sendo solta nele.  <br/> |
|FALSE  <br/> |A forma não pode ser solta no grupo.  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir esse valor selecionando o grupo, clicando em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e marcando a caixa de seleção **Aceitar formas soltas**. 
  
Para adicionar uma forma soltando-a no grupo, você também deve ativar um comportamento de forma semelhante. Selecione a forma, clique em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, marque a caixa de seleção **Adicionar forma aos grupos ao soltar**. Esse valor será armazenado na célula IsDropSource na seção Miscellaneous. 
  
Para obter uma referência para a célula IsDropTarget pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |IsDropTarget  <br/> |
   
Para obter uma referência para a célula IsDropTarget pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowGroup** <br/> |
|Índice de célula:  <br/> |**visGroupIsDropTarget** <br/> |
   

