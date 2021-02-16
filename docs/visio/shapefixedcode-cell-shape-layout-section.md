---
title: Célula ShapeFixedCode (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Especifica o comportamento de posicionamento de uma forma de colocação.
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431740"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>Célula ShapeFixedCode (Seção Shape Layout)

Especifica o comportamento de posicionamento de uma forma de colocação.
  
|**Valor**|**Modo de seleção**|**Constante de automação**|
|:-----|:-----|:-----|
|&amp;H1  <br/> |Não mova essa forma quando as formas são formadas usando a caixa de diálogo Configurar **Layout.**  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |Não mover esta forma e não permitir que as formas ajustadas sejam colocadas em cima dela.  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |Não mover esta forma e permitir que as formas ajustadas sejam colocadas em cima dela.  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |Ignorar localizações de ponto de conexão durante o roteamento.  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |Permitir somente o roteamento para lados com pontos de conexão.  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |Não cola ao perímetro dessa forma. Em vez disso, cola à caixa de alinhamento da forma.  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula  na guia Posicionamento na caixa [](run-in-developer-mode-display-the-developer-tab.md) de diálogo Comportamento (com uma forma selecionada,  na guia Desenvolvedor, no grupo **Design** da Forma, clique em Comportamento e na guia Posicionamento).   
  
Você pode definir qualquer combinação desses valores para a célula. Por exemplo, você pode inserir o valor 3 ( H3), que elimina o movimento quando você forma o layout usando a caixa de diálogo Configurar Layout (na guia &amp; **Design,** no grupo **Layout,** clique em **Re-Layout Page** e em Mais Opções de **Layout** ) e quando outras formas de colocação são colocadas na forma ou perto dela.  
  
Nas versões do Visio anteriores ao Visio 2000, esse comportamento era definido por meio da célula ObjInteract na seção Miscellaneous. 
  
Para obter uma referência à célula ShapeFixedCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapeFixedCode  <br/> |
   
Para obter uma referência para a célula ShapeFixedCode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice de célula:  <br/> |**visSLOFixedCode** <br/> |
   

