---
title: Célula ShapePermeablePlace (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Determina se formas de colocação podem ser posicionadas na parte superior de uma forma ao dispor as formas na caixa de diálogo Configurar Layout (na guia Design, do grupo Layout, clique em Refazer o Layout da Página e em Mais Opções de Layout).
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427217"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>Célula ShapePermeablePlace (Seção Shape Layout)

Determina se formas de colocação podem ser posicionadas na parte superior de uma forma ao dispor as formas na caixa de diálogo **Configurar Layout** (na guia **Design**, do grupo **Layout**, clique em **Refazer o Layout da Página** e em **Mais Opções de Layout**).
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Permitir que as formas sejam colocadas em cima de uma forma.  <br/> |
|FALSE  <br/> |Não permitir que as formas sejam colocadas em cima de uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula  na guia Posicionamento na caixa [](run-in-developer-mode-display-the-developer-tab.md) de diálogo Comportamento (com uma forma selecionada,  na guia Desenvolvedor, no grupo **Design** da Forma, clique em Comportamento e na guia Posicionamento).   
  
Nas versões do Visio anteriores ao Visio 2000, esse comportamento era definido por meio da célula ObjInteract na seção Miscellaneous.
  
Para obter uma referência para a célula ShapePermeablePlace pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapePermeablePlace  <br/> |
   
Para obter uma referência para a célula ShapePermeablePlace pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice de célula:  <br/> |**visSLOPermeablePlace** <br/> |
   

