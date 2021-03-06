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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405447"
---
# <a name="visible-cell-layers-section"></a>Célula Visible (Seção Layers)

Especifica se as formas pertencentes à camada ficarão visíveis na página de desenho.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |As formas são visíveis.  <br/> |
|FALSE  <br/> |As formas estão ocultas.  <br/> |
   
## <a name="remarks"></a>Comentários

Essa célula corresponde à opção  Visível na caixa de  diálogo Propriedades  da Camada (na guia Início, no grupo Edição, clique em Camadas e em Propriedades da **Camada).**   
  
Para obter uma referência para a célula Visible pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers.Visible[ *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Visible pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice de linha:  <br/> |**visRowLayer**  +   *i* onde *i* = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visLayerVisible** <br/> |
   

