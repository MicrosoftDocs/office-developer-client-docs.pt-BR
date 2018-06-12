---
title: Célula Active (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Especifica se a camada está ativa. As formas sem camadas atribuídas previamente são atribuídas à(s) camada(s) ativa(s) quando você as arrasta para a página de desenho.
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771250"
---
# <a name="active-cell-layers-section"></a>Célula Active (Seção Layers)

Especifica se a camada está ativa. As formas sem camadas atribuídas previamente são atribuídas à(s) camada(s) ativa(s) quando você as arrasta para a página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A camada está ativa.  <br/> |
|FALSO  <br/> |A camada não está ativa.  <br/> |
   
## <a name="remarks"></a>Coment�rios

O valor desta célula corresponde à configuração **ativa** na caixa de diálogo **Propriedades da camada** (no grupo **edição** na guia **página inicial** , clique em **camadas**e, em seguida, clique em **Propriedades da camada**).
  
Para obter uma referência à célula Active pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers.Active [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência à célula Active pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice da linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visLayerActive** <br/> |
   

