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
ms.openlocfilehash: f97f7dc09d1f882452ae2234882de45f06bd0da1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417431"
---
# <a name="active-cell-layers-section"></a>Célula Active (Seção Layers)

Especifica se a camada está ativa. As formas sem camadas atribuídas previamente são atribuídas à(s) camada(s) ativa(s) quando você as arrasta para a página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |A camada está ativa.  <br/> |
|FALSE  <br/> |A camada não está ativa.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor nesta célula corresponde à opção **Ativo** na caixa de diálogo **Propriedades da Camada** (no grupo **Edição** na guia **Página Inicial**, clique em **Camadas** e em **Propriedades da Camada**).
  
Para fazer referência à célula Active pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers.Active[ *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para fazer referência à célula Active pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice de linha:  <br/> |**visRowLayer**  +   *i* onde *i* = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visLayerActive** <br/> |
   

