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
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772887"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>Célula ShapePermeablePlace (Seção Shape Layout)

Determina se formas de colocação podem ser posicionadas na parte superior de uma forma ao dispor as formas na caixa de diálogo **Configurar Layout** (na guia **Design**, do grupo **Layout**, clique em **Refazer o Layout da Página** e em **Mais Opções de Layout**).
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Permitir que as formas sejam colocadas em cima de uma forma.  <br/> |
|FALSO  <br/> |Não permitir que as formas sejam colocadas em cima de uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com a forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **Design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ). 
  
Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjInteract, na seção Miscellaneous, para definir esse comportamento.
  
Para obter uma referência para a célula ShapePermeablePlace pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapePermeablePlace  <br/> |
   
Para obter uma referência para a célula ShapePermeablePlace pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOPermeablePlace** <br/> |
   

