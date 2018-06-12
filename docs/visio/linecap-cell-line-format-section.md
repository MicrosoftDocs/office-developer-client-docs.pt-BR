---
title: Célula LineCap (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Indica se as terminações da linha são arredondadas, quadradas ou estendidas.
ms.openlocfilehash: 1bd427801e6d95ce6167fa9681da2c567307f072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772195"
---
# <a name="linecap-cell-line-format-section"></a>Célula LineCap (Seção Line Format)

Indica se as terminações da linha são arredondadas, quadradas ou estendidas.
  
|**Valor**|**Estilo do fim de linha**|
|:-----|:-----|
|0  <br/> |Arredondado  <br/> |
|1  <br/> |Quadrado  <br/> |
|2  <br/> |Estendido  <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula na caixa de diálogo **linha** (na guia **página inicial** , no grupo **forma** , clique em **linha**, aponte para **setas**e, em seguida, clique em **Mais setas**).
  
Para obter uma referência para a célula LineCap pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineCap  <br/> |
   
Para obter uma referência para a célula LineCap pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowLine** <br/> |
|Índice da célula:  <br/> |**visLineEndCap** <br/> |
   

