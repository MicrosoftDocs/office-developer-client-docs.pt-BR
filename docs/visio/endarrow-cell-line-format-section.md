---
title: Célula EndArrow (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Indica se a linha tem uma ponta de seta ou outro formato de fim de linha em seu último vértice.
ms.openlocfilehash: 54ef11125a8774914a60897850fb75cd4ab949a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434680"
---
# <a name="endarrow-cell-line-format-section"></a>Célula EndArrow (Seção Line Format)

Indica se a linha tem uma ponta de seta ou outro formato de fim de linha em seu último vértice.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Sem ponta de seta.  <br/> |
|1 - 45  <br/> |Estilos de ponta de seta variados correspondentes a entradas indexadas na caixa de diálogo **Linha**.  <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir esse valor na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Setas** e em **Mais Setas**). O tamanho da ponta de seta é definido na célula EndArrowSize.
  
Você pode especificar um fim de linha personalizado utilizando a função USE nesta célula. 
  
Para obter uma referência para a célula EndArrow pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |EndArrow  <br/> |
   
Para obter uma referência para a célula EndArrow pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowLine** <br/> |
|Índice de célula:  <br/> |**visLineEndArrow** <br/> |
   

