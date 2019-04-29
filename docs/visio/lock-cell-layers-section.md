---
title: Célula Lock (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Especifica se as formas pertencentes à camada estão protegidas contra seleção ou edição.
ms.openlocfilehash: d548a6f0fe0cac10d80d73c904739b2979ecf27f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438824"
---
# <a name="lock-cell-layers-section"></a>Célula Lock (Seção Layers)

Especifica se as formas pertencentes à camada estão protegidas contra seleção ou edição.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |As formas estão protegidas.  <br/> |
|FALSE  <br/> |As formas não estão protegidas.  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir esse valor selecionando a opção **Bloquear** na caixa de diálogo **Propriedades da Camada** (na guia **Página Inicial** no grupo **Edição** clique em **Camadas** e em **Propriedades da Camada**).
  
Para obter uma referência para a célula Lock pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Layers. Locked [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Lock pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionLayer** <br/> |
|Índice de linha:  <br/> |**visRowLayer** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visLayerLock** <br/> |
   

