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
ms.openlocfilehash: 6ae83fa70cc545c88080ce27046bd8c226c060e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772878"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>Célula ShapeFixedCode (Seção Shape Layout)

Especifica o comportamento de posicionamento de uma forma de colocação.
  
|**Valor**|**Modo de seleção**|**Constante de automação**|
|:-----|:-----|:-----|
|&amp;H1  <br/> |Não mova esta forma quando as formas forem dispostas usando a caixa de diálogo **Configurar Layout** .  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |Não mover esta forma e não permitir que as formas ajustadas sejam colocadas em cima dela.  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |Não mover esta forma e permitir que as formas ajustadas sejam colocadas em cima dela.  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |Ignorar localizações de ponto de conexão durante o roteamento.  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |Permitir somente o roteamento para lados com pontos de conexão.  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |Não associar ao perímetro desta forma, mas à caixa de alinhamento da forma.  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com a forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **Design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ). 
  
Você pode definir qualquer combinação desses valores para essa célula. Por exemplo, você pode inserir o valor 3 (&amp;H3), que elimina o movimento ao dispor formas usando a caixa de diálogo **Configurar Layout** (na guia **Design** , no grupo **Layout** , clique em **Novo Layout de página**e, em seguida, clique em ** Mais opções de Layout** ) e quando outras formas de colocação são inseridas ou perto da forma. 
  
Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjInteract, na seção Miscellaneous, para definir esse comportamento. 
  
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
   

