---
title: Célula Visible (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Especifica se as formas pertencentes à camada ficarão visíveis na página de desenho.
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357810"
---
# <a name="visible-cell-layers-section"></a>Célula Visible (Seção Layers)

Especifica se as formas pertencentes à camada ficarão visíveis na página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |As formas são visíveis.  <br/> |
|FALSE  <br/> |As formas estão ocultas.  <br/> |
   
## <a name="remarks"></a>Comentários

Esta célula corresponde à opção **visível** na caixa de diálogo **Propriedades da camada** (na guia **página inicial** , no grupo **edição** , clique em **camadas**e em Propriedades da **camada** ). 
  
Para obter uma referência para a célula Visible pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers. Visible [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Visible pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice da linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visLayerVisible** <br/> |
   

