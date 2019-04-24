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
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326513"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>Célula ShapePermeableY (Seção Shape Layout)

Determina se um conector pode fazer o roteamento verticalmente por uma forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |Permitir que os conectores façam o roteamento verticalmente por uma forma.  <br/> |
|FALSE  <br/> |Não permitir que os conectores façam o roteamento verticalmente por uma forma.  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com uma forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ). 
  
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
   

