---
title: Célula IsDropSource (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Determina se a forma pode ser adicionada ao grupo sendo solta nele.
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360169"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>Célula IsDropSource (Seção Miscellaneous)

Determina se a forma pode ser adicionada ao grupo sendo solta nele.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |A forma pode ser adicionada ao grupo sendo solta nele.  <br/> |
|FALSE  <br/> |A forma não pode ser adicionada ao grupo.  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir esse valor selecionando a forma, clicando em **Comportamento** na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e marcando a caixa de seleção **Adicionar forma aos grupos ao soltar**. 
  
Além de ativar esse comportamento para uma forma, também é necessário ativar um grupo que aceite formas arrastadas para dentro dele. Para fazer isso, clique em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e, em seguida, marque a caixa de seleção **Aceitar formas soltas**. Este valor será armazenado na célula IsDropTarget na seção Group Properties. 
  
Para obter uma referência para a célula IsDropSource pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |IsDropSource  <br/> |
   
Para obter uma referência para a célula IsDropSource pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowMisc** <br/> |
|Índice da célula:  <br/> |**visDropSource** <br/> |
   

