---
title: Célula ShapePermeableX (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Determina se um conector pode fazer o roteamento horizontalmente por uma forma de colocação.
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357047"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>Célula ShapePermeableX (Seção Shape Layout)

Determina se um conector pode fazer o roteamento horizontalmente por uma forma de colocação.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |Permitir que os conectores façam o roteamento horizontalmente por uma forma de colocação.  <br/> |
|FALSE  <br/> |Não permitir que os conectores façam o roteamento horizontalmente por uma forma de colocação.  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com uma forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ). 
  
Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjInteract, na seção Miscellaneous, para definir esse comportamento. 
  
Para obter uma referência para a célula ShapePermeableX pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapePermeableX  <br/> |
   
Para obter uma referência para a célula ShapePermeableX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOPermX** <br/> |
   

