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
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425194"
---
# <a name="linecap-cell-line-format-section"></a>Célula LineCap (Seção Line Format)

Indica se as terminações da linha são arredondadas, quadradas ou estendidas.
  
|**Valor**|**Estilo do fim de linha**|
|:-----|:-----|
|0  <br/> |Arredondado  <br/> |
|1   <br/> |Quadrado  <br/> |
|2   <br/> |Estendida  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o valor dessa célula na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Setas** e em **Mais Setas**).
  
Para obter uma referência para a célula LineCap pelo nome, a partir de outra célula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineCap  <br/> |
   
Para obter uma referência para a célula LineCap a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowLine** <br/> |
|Índice de célula:  <br/> |**visLineEndCap** <br/> |
   

