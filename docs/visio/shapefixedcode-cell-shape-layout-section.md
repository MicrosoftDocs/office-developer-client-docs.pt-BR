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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325729"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>Célula ShapeFixedCode (Seção Shape Layout)

Especifica o comportamento de posicionamento de uma forma de colocação.
  
|**Valor**|**Modo de seleção**|**Constante de automação**|
|:-----|:-----|:-----|
|&amp;Semestre  <br/> |Não mover esta forma quando as formas forem projetadas usando a caixa de diálogo **Configurar layout** .  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;S2  <br/> |Não mover esta forma e não permitir que as formas ajustadas sejam colocadas em cima dela.  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |Não mover esta forma e permitir que as formas ajustadas sejam colocadas em cima dela.  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |Ignorar localizações de ponto de conexão durante o roteamento.  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |Permitir somente o roteamento para lados com pontos de conexão.  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |Não associe ao perímetro desta forma. Associe à caixa de alinhamento da forma.  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com uma forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ). 
  
Você pode definir qualquer combinação desses valores para a célula. Por exemplo, você pode inserir o valor 3 (&amp;H3), que elimina o movimento ao dispor formas usando a caixa de diálogo **Configurar layout** (na guia **design** , no grupo **layout** , clique em refazer o **layout da página**e, em seguida, clique em ** Mais opções de layout** ) e quando outras formas posicionáveis são colocadas na forma ou ao lado dela. 
  
Nas versões do Visio anteriores ao Visio 2000, esse comportamento era definido por meio da célula ObjInteract na seção Miscellaneous. 
  
Para obter uma referência à célula ShapeFixedCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapeFixedCode  <br/> |
   
Para obter uma referência para a célula ShapeFixedCode pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOFixedCode** <br/> |
   

