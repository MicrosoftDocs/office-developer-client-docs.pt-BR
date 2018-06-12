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
description: Especifica se as formas pertencentes à camada serão visíveis na página de desenho.
ms.openlocfilehash: 9a025403b1f5b46d2f439805a15954eaeeab2686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773255"
---
# <a name="visible-cell-layers-section"></a>Célula Visible (Seção Layers)

Especifica se as formas pertencentes à camada serão visíveis na página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |As formas são visíveis.  <br/> |
|FALSO  <br/> |As formas estão ocultas.  <br/> |
   
## <a name="remarks"></a>Comentários

Essa célula corresponde à opção **visível** na caixa de diálogo **Propriedades da camada** (na guia **página inicial** , no grupo **edição** , clique em **camadas**e, em seguida, clique em **Propriedades da camada** ). 
  
Para obter uma referência para a célula Visible pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers.Visible [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência para a célula Visible pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice da linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visLayerVisible** <br/> |
   

