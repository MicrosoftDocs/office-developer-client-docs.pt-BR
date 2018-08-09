---
title: Célula ShapePermeableY (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Determina se um conector pode fazer o roteamento verticalmente por uma forma.
ms.openlocfilehash: 4a7a389ec1d753b8582b7ff0b921a615e582b1ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772884"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>Célula ShapePermeableY (Seção Shape Layout)

Determina se um conector pode fazer o roteamento verticalmente por uma forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Permitir que os conectores façam o roteamento verticalmente por uma forma.  <br/> |
|FALSO  <br/> |Não permitir que os conectores façam o roteamento verticalmente por uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com a forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **Design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ). 
  
Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjInteract, na seção Miscellaneous, para definir esse comportamento.
  
Para obter uma referência para a célula ShapePermeableY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShapePermeableY  <br/> |
   
Para obter uma referência para a célula ShapePermeableY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLOPermY** <br/> |
   

