---
title: Célula Print (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Especifica se as formas pertencentes à camada podem ser impressas.
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356179"
---
# <a name="print-cell-layers-section"></a>Célula Print (Seção Layers)

Especifica se as formas pertencentes à camada podem ser impressas.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |As formas podem ser impressas.  <br/> |
|FALSE  <br/> |As formas não podem ser impressas.  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir esse valor usando a opção **Imprimir** na caixa de diálogo **Propriedades da Camada** (na guia **Página Inicial** no grupo **Edição** clique em **Camadas** e em **Propriedades da Camada**).
  
Para obter uma referência para a célula Print pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers. Print [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Print pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice da linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visDocPreviewScope** <br/> |
   

