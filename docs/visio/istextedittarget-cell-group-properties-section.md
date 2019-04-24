---
title: Célula IsTextEditTarget (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Determina a atribuição de texto de um grupo.
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314914"
---
# <a name="istextedittarget-cell-group-properties-section"></a>Célula IsTextEditTarget (Seção Group Properties)

Determina a atribuição de texto de um grupo.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |O texto é adicionado à forma do grupo.  <br/> |
|FALSE  <br/> |O texto é adicionado à forma do grupo no início da ordem de empilhamento.  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir esse valor selecionando o grupo, clicando em **Comportamento**, na guia [Desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) e marcando a caixa de seleção **Editar texto do grupo**. 
  
Os grupos criados em versões anteriores ao Visio 2000 têm um valor padrão de FALSO. A partir do Visio versão 2000, o valor padrão é VERDADEIRO. 
  
Para obter uma referência para a célula IsTextEditTarget pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |IsTextEditTarget  <br/> |
   
Para obter uma referência para a célula IsTextEditTarget pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowGroup** <br/> |
|Índice da célula:  <br/> |**visGroupIsTextEditTarget** <br/> |
   

